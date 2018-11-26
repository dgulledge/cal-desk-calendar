# cal-desk-calendar
Desk calendar style extensions to Emacs' Calendar/Diary

This is an extension to the existing Emacs Diary display.  It formats the
entries like a desk calendar.  On a normal desk calendar each row represents
a fixed amount of time during the day, typically either 15 of 30 minutes or
an entire hour.  That's the default if everything fits, but rows with too much
to fit are expanded, and events that occur at specific times that don't fall
on the stated boundaries get their own row.  The screenshot below gives some
idea as to how this looks.

See the comments at the beginning of cal-desk-calendar.el for a detailed
explanation of the configuration options.  The short version is that you can
just load cal-desk-calendar.el and set a couple of hooks:
```
    (load-library "cal-desk-calendar")
    (add-hook 'diary-display-hook 'sort-diary-entries)
    (add-hook 'diary-display-hook 'fancy-schedule-display-desk-calendar t)
```
There are additional settings for the length of intervals, time for the start
and end of your normal workday, the time format you prefer, etc.

![screenshot](/Emacs-Desk-Calendar-screenshot.png "Emacs Desk Calendar screenshot")
