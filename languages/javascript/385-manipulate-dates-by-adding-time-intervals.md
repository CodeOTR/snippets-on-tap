# Manipulate Dates by Adding Time Intervals

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/385)
  
  ## Code Snippet
  ```
  // addSecondsToDate(new Date('2020-10-19 12:00:00'), 10);
const addSecondsToDate = (date, n) => {
  const d = new Date(date);
  d.setTime(d.getTime() + n * 1000);
  return d;
};

// addMinutesToDate('2020-10-19 12:00:00', 10);
const addMinutesToDate = (date, n) => {
  const d = new Date(date);
  d.setTime(d.getTime() + n * 60_000);
  return d;
};

// addHoursToDate('2020-10-19 12:00:00', 10);
const addHoursToDate = (date, n) => {
  const d = new Date(date);
  d.setTime(d.getTime() + n * 3_600_000);
  return d;
};

// addDaysToDate('2020-10-15', 10);
const addDaysToDate = (date, n) => {
  const d = new Date(date);
  d.setDate(d.getDate() + n);
  return d;
};


const isWeekday = date => date.getDay() % 6 !== 0;

const addWeekDays = (date, n) => {
  const s = Math.sign(n);
  const d = new Date(date);
  return Array.from({ length: Math.abs(n) }).reduce((currentDate) => {
    currentDate = addDaysToDate(currentDate, s);
    while (!isWeekday(currentDate))
      currentDate = addDaysToDate(currentDate, s);
    return currentDate;
  }, d);
};
  ```
  
  ## Description
  The code snippet you provided is a set of utility functions for manipulating JavaScript dates.

The **addSecondsToDate** function takes a date and a number of seconds to add, and returns a new date that is the specified number of seconds later.

The **addMinutesToDate** function is similar, but it takes a number of minutes to add instead of seconds.

The **addHoursToDate** function takes a number of hours to add instead of minutes.

The **addDaysToDate** function takes a number of days to add instead of hours.

The **isWeekday** function takes a date and returns a boolean indicating whether or not the date is a weekday (Monday through Friday).

The **addWeekDays** function takes a date and a number of weekdays to add, and returns a new date that is the specified number of weekdays later.

These functions can be useful for a variety of date-related tasks, such as scheduling appointments, calculating due dates, or finding the next business day.
  
  ## Tags
  javascript, date, date-manipulation, date-formatting, date-time, date-arithmetic
