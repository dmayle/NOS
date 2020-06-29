# Update Mechanism
This contains the documentation on the update mechanism

The current plan is to borrow as much learning as possible from ChromeOS
 * https://www.chromium.org/chromium-os/chromiumos-design-docs/filesystem-autoupdate
 * https://www.chromium.org/chromium-os/chromiumos-design-docs/autoupdate-details

There is one noticeable difference, which is we plan to use time rather than boot counts in order to prevent bad boots from bricking the install.  On upgrade, we'll add add an update time window during which booting will work.  Assuming that boot works, this will be marked as such.  If not, time will expire and the previous boot will combe back.
