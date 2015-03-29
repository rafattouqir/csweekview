# CSWeekView #
This is a set of three Cocoa classes (subclasses of NSView) that together organize and display a weekly calendar, organized horizontally.

## CSWeekView ##
This is the singleton "parent" view; it contains five CSDayViews, from top to bottom, each the full width of the CSWeekView.  Each CSDayView contains a variable number of CSEventViews.
The CSWeekView will resize itself vertically to accommodate the needed expansion of the CSDayViews, which may not overlap with each other.
This is responsible for drawing headers (hour labels) and vertical boundaries between hours.
CSWeekView expects to receive events as a 5-member NSArray (one per day).  Each member is itself an NSArray of NSDictionaries, each of which represents the details for a single event.
Start times and durations are handled as integers; the number of minutes that correspond to a time unit is specified in the CSWeekView.h header.  In my conception (and the demo), each represents a half-hour, but it could be different for you.

## CSDayView ##
Each of these represents a day of the week, and is responsible for organizing the CSEventViews spatially.

## CSEventView ##
Records and displays information for a single event.

## CSWeekView Demo ##
This is a demo project showing how the WeekView works.