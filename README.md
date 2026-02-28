Upcoming Potential Features

Update Search and Sort to be more refined:
Sort by release year.
Keyword Search?
Movies/TV Series/Collections filter by genre, rating, etc. 
Search or filter based on specific metadata: genre, rating, maybe actors, etc. 
There needs a dropdown under search bar that is associaed with Tab's different views, for Movies and Other it would be All, Playlists, and Collections, TV Series its nothing, Music its all the ones in the dropdown. 


Casting:
Airplay casting capability?

Metadata and images:
Artwork moving folder 
Embedded Image Extractor
.nfo files, stored in location or stored in a separate folder? (Auto-export after search, after successful online search?)
Hold and drag for metadata and image fetchers to  increase or decrease the priority compared to the other enabled metadata or image fetchers. 
Setting at initial builld, Or saving opens up setting and doesn't start scan until save for the first time?

Libraries:
Smart Collection: tags, Ratings, etc.
Password protected library for webpage viewing
Add ability to access Onedrive, Google Drive, and Network storage for adding folders. Remote storage being displayed on side where folder selection is. 
Setting to ignore hero image at top of main pages

Audiobooks:
Create an audiobooks library type. Continue listening will be shown in Audiobooks library types.  Audiobookshelf.
🔑 Primary Metadata Sources Used by Audiobook Apps
📚 Open Library (MOST IMPORTANT)
This is the backbone for Audiobookshelf and similar projects.

Other:
Other Hover for preview/trailer
Other based metadata and images have it specify an option to set Adult in the fetch 

Photos:
Photos change every 5 seconds in photoviewer?
Two finger spread functionality to Zoom in and out in the photo viewer. 
Photos face scanning for collection creation, etc. Tie in an AI?
Search working

Music:
Display name is AudioDB found name not directory name for Albums
Android Auto?
How to get the top hits of an album
Enrich Artist page to show artist metadata about Artist. 
Make Playlist creation easier by putting it in Music Library pages?
Karaoke style add to queue capability for Party Playlist
Drag and drop order = for Queue, might be hard with DB write being integrated already.
Radio style mixes

Way to use a Sonic analyzer for creating playlists:
Implementation Concepts (High-Level, No Code)
1) Define the “Seed”
Pick a starting point:
Track, artist, album, or playlist.
Optionally use multiple seeds for “blend” mixes.
2) Build a Candidate Pool
You’ll need a set of tracks that could plausibly belong in the mix:
Same artist or album (core relevance).
Similar genres (if tags exist in metadata).
Recently added / popular (if you track play counts).
User favorites (if you track likes or ratings).
If your library data is mostly local, you can base this on:
Artist/album metadata you already have.
File structure (artist/album hierarchy).
Optional user-defined tags or “moods” you can add later.
3) Scoring & Ranking
Create a relevance score to rank candidates. A simple weighted scoring model works well:
Artist match = high weight.
Same album = medium weight (if album radio is desired).
Genre overlap = medium weight.
User behavior = boost for liked, penalize for skipped.
4) Enforce Variety
To prevent repetition:
Avoid repeating the same artist too soon.
Limit tracks from a single album in a short window.
Add diversity constraints such as “no more than 2 tracks from same artist in last 10”.
5) Generate in Batches
Instead of building a huge queue:
Generate 10–20 tracks at a time.
Recompute when the user skips or finishes a batch.
This keeps the mix adaptive.
6) Feedback Loop
Track user actions:
Skip → reduce weight for that track/artist.
Like/Favorite → boost relevance for similar tracks.
Replay → increase weight.
Even a lightweight feedback loop makes the radio feel more “personal”.


TV Series:
Add TMDB search for Main Series' trailer?
Theme songs, with setting for turning on/off?
Ability to mark episode watched and have it show continue watching.

Karaoke:
Remove the countdown on the "Karaoke default video"

Security: 
Only accessible with code, ways to lock out for too many incorrect attempts. User approve it on app. (Removes button, if command for API request?) 
Future https self signed cause it's only local files, so maybe. 
Specific LAN access (future for Firewall protection) 

Users:
Users with accounts and Library access (this is resource dependent) Rule for number of users.)
User rating setting.

Backup:
Import/export collections
Backup feature for DB
Trakt

Settings:
In the Settings section, I want there to be a Home Details Setting where the admin can change the order of the libraries being shown on the home page. 
Languages (tie google translate to it?) tie things like TMDB language selection for API calls.
Add a system resource monitoring capability (CPU/RAM) 
Add a Country of origin specifier in Settings for ratings.
Make sure logs 

Appearance:
Display changes/Branding
Card sizes - list, grid, Poster
User interface Languages
Continue watching show full image cards?
