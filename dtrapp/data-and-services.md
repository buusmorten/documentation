# DTRAPP Data and Service Overview

Last updated: July 31, 2026

| Function | Data involved | Destination | User control |
|---|---|---|---|
| Live radio | Stream request and ordinary network metadata | SAM Cloud / Spacial | Start or stop playback |
| Station information | Program, track, artwork, and schedule requests | Den Tunge Radio and station services | Use or close the app |
| Podcasts | Selected podcast link | Mixcloud through the browser | User explicitly opens the link |
| Saved tracks | Track metadata | Device and optional private iCloud | Save, unsave, or manage iCloud |
| Listening statistics | Listening duration and aggregate local counters | Device and optional private iCloud | Stored as private app data |
| Program reminders | Selected program and reminder schedule | Device / Apple notification system | Permission and in-app toggle |
| Aggregate track saves | Track metadata, time, app version, platform, source | Den Tunge Radio Supabase project | Generated only for saved-track aggregation |
| Widget and Live Activity | Current station and Now Playing presentation | Apple system surfaces / app group | Add/remove widget; stop playback |

The Supabase publishable key included in the app is a public client credential, not a
database administrator secret. Backend authorization and row-level security must
remain correctly configured by the service operator.

See the [Privacy Policy](privacy.md) for the complete disclosure.
