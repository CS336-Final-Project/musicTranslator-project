# Project Design
## Preliminary Design
## Description of Components
- Song Lyrics Component
  - Purpose:
    - Displays the lyrics of the current song along with translations in the user’s preferred learning languages
    - Will display the orignal lyrics on one side & the translated lyrics on the other
  - Data Maintained:
    - songID(string): ID of the current song
    - lyrics(string): Orignal lyrics of the song
    - translations(object): Key-value pair of translations(languageCode: translatedLyrics)
    - currentLanguage(string): Selected language for viewing lyrics
  - API Made Available:
    - 
- Player Component
  - Purpose:
    - Provides controls for music playback, including play, pause, skip, and volume adjustments
    - Displays the current playback progress and allows the user to seek within the track
  - Data Maintained:
    - isPlaying(boolean): Indicates whether the song is currently playing
    - currentTime(number): Current playback time in seconds or mintues & seconds
    - totalDuration(number): Total duration of the track in seconds or minutes & seconds
    - songID(string): ID of the current song
  - API Made Available:
    - 
- MusicCardComponent
  - Purpose:
    - Displays track or artist information in a visually appealing card format
    - Allows users to mark songs as "liked" or add them to their learning list
  - Data Maintained:
    - songID(string): ID of the song represented by the card
    - songName(string): Name of the song represented by the card
    - artistName(string): Name of the artist represented by the card
    - albumnArt(string): URL of the album artwork image
  - API Made Available:
- Search Bar Component:
  - Purpose:
    - Allows users to search for songs, artists, or genres.
    - Suggests results dynamically as the user types.
  - Data Maintained:
    - query(string): The current query entered by the user
    - searchResults(array of strings): Array of results matching the query
  - API Made Available:

## DB Structure
### Collections & Documents
- users
   - userID
      - name
      - primaryLanguage
      - learningLanguages
      - recentListen
         - listenID01
         - listenID02
         - ...
      - likedSongs
         - likedSong01
         - likedSong02
         - ...
      - recentSearches
         - searchID01
         - searchID02

[Example](https://github.com/CS336-Final-Project/musicTranslator-project/blob/main/Docs/DBstructure.png)

## Implementation Plan
1. Create the nav bar & pages
2. Implement the authorization component/sign into Spotify
3. Integrate the Spotify API & MusixMatch API into our application(test to make sure we get resutls)
4. Integrate Firebase into our application
5. Build the components into our application & design the pages
  - Home Page:
    - Search Component
    - Top Tracks Card Component 
    - Top Artist Card Component
  - Search Page:
    - Search Component
    - Recommendation Component
  - Listen Page:
    - Lyrics Component
    - Playback Component
  - Profile Page:
    - ...
6. Style components and finalize user interactions

## Team Responsibilities
- Tyler
  - Set up routing
  - Set up Spotify & MusixMatch API
  - Create API calls to retrieve user information
- Ha Dong
  - Work on Search & Profile Page
