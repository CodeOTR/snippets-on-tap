# utils_calendar.dart

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/375)
  
  ## Code Snippet
  ```
  import 'package:add_2_calendar/add_2_calendar.dart';
import 'package:flutter/material.dart';
import 'package:intl/intl.dart';
import 'package:url_launcher/url_launcher.dart';

class CalendarUtils {
  static void showCalendarPopup(BuildContext context, Event event) {
    final Size screenSize = MediaQuery.of(context).size;

    showMenu(
      context: context,
      position: RelativeRect.fromLTRB(screenSize.width / 2 - 50,
          screenSize.height / 2 - 100, screenSize.width, screenSize.height),
      shape: const RoundedRectangleBorder(
          borderRadius: BorderRadius.all(Radius.circular(10))),
      items: [
        PopupMenuItem(
          child: Row(
            children: [
              Image.asset('assets/images/icon_calendar_google_128x.png',
                  width: 24, height: 24),
              const SizedBox(width: 8),
              const Text('Google'),
            ],
          ),
          onTap: () {
            String url = CalendarUtils.generateGoogleCalendarUrl(event);

            launchUrl(Uri.parse(url), mode: LaunchMode.externalApplication);
          },
        ),
        PopupMenuItem(
          child: Row(
            children: [
              Image.asset('assets/images/icon_calendar_outlook_128x.png',
                  width: 24, height: 24),
              const SizedBox(width: 8),
              const Text('Outlook'),
            ],
          ),
          onTap: () {
            String url = CalendarUtils.generateOutlookCalendarUrl(event);

            launchUrl(Uri.parse(url), mode: LaunchMode.externalApplication);
          },
        ),
        PopupMenuItem(
          child: Row(
            children: [
              Image.asset('assets/images/icon_calendar_yahoo_128x.png',
                  width: 24, height: 24),
              const SizedBox(width: 8),
              const Text('Yahoo'),
            ],
          ),
          onTap: () {
            String url = CalendarUtils.generateYahooCalendarUrl(event);

            launchUrl(Uri.parse(url), mode: LaunchMode.externalApplication);
          },
        ),
        PopupMenuItem(
          child: Row(
            children: [
              Image.asset('assets/images/icon_calendar_ios_128x.png',
                  width: 24, height: 24),
              const SizedBox(width: 8),
              const Text('Save to device'),
            ],
          ),
          onTap: () {
            Add2Calendar.addEvent2Cal(event);
          },
        ),
      ],
    );
  }

  static String generateGoogleCalendarUrl(Event event) {
    String formattedStartDate =
        DateFormat('yyyyMMdd\'T\'HHmmss\'Z\'').format(event.startDate);
    String formattedEndDate =
        DateFormat('yyyyMMdd\'T\'HHmmss\'Z\'').format(event.endDate);

    String url =
        'https://www.google.com/calendar/render?action=TEMPLATE&text=${event.title}'
        '&details=${event.description}&location=${event.location}&dates=$formattedStartDate/$formattedEndDate';

    return url;
  }

  static String generateOutlookCalendarUrl(Event event) {
    String formattedStartDate =
        DateFormat('yyyy-MM-dd\'T\'HH:mm:ss\'Z\'').format(event.startDate);
    String formattedEndDate =
        DateFormat('yyyy-MM-dd\'T\'HH:mm:ss\'Z\'').format(event.endDate);

    String url =
        'https://outlook.live.com/calendar/deeplink/compose?path=/calendar/action/compose&rru=addevent'
        '&startdt=$formattedStartDate'
        '&enddt=$formattedEndDate'
        '&subject=${event.title}'
        '&body=${event.description}'
        '&location=${event.location}';

    return url;
  }

  static String generateYahooCalendarUrl(Event event) {
    String formattedStartDate =
        DateFormat('yyyyMMdd\'T\'HHmmss\'Z\'').format(event.startDate);
    String formattedEndDate =
        DateFormat('yyyyMMdd\'T\'HHmmss\'Z\'').format(event.endDate);

    String url =
        'https://calendar.yahoo.com/?v=60&view=d&type=20&title=${event.title}'
        '&st=$formattedStartDate&et=$formattedEndDate&desc=${event.description}&in_loc=${event.location}';

    return url;
  }
}

  ```
  
  ## Description
  **Explanation:**
This code snippet provides a set of functions that allow you to easily add events to various calendar applications.

**CalendarUtils class:**
This class contains various methods to interact with calendar applications.

**showCalendarPopup() method:**
This method displays a menu of options to add the current event to different calendar applications, including Google, Outlook, Yahoo, and the device's native calendar. It is typically called when the user clicks a button or icon to add an event to their calendar.

**generateGoogleCalendarUrl(), generateOutlookCalendarUrl(), generateYahooCalendarUrl() methods:**
These methods generate specific URLs for adding the event to the respective calendar applications. They format the event details (title, description, location, start and end dates) into a format that is compatible with each application's API.

**launchUrl() method:**
This method is used to launch a URL in an external application, such as a browser or calendar app. It is called to open the generated calendar URLs in the appropriate applications.

**Event class:**
This class represents an event with properties like title, description, location, start date, and end date.

**Usage:**
To use these utility functions, you can initialize an Event object with your event details and then call the showCalendarPopup() method with the event object as an argument. This will display the menu of calendar applications to which the event can be added.

This utility class simplifies the process of adding events to different calendar applications and provides a user-friendly way for users to save events to their preferred calendar of choice.
  
  ## Tags
  dart, flutter, android
