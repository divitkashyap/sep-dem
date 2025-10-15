# 2024-PlaylistGuitarLessons
#

2024-PlaylistGuitarLessons is a web application designed to help aspiring guitarists learn their favorite songs in a personalized and engaging way. Key features include integration with Spotify, allowing users to pull songs directly from their playlists or input them manually via a text box. The app utilizes web scraping techniques to gather guitar tabs and chord charts for these songs, which are then organized by difficulty level through an algorithm. This ensures that users can practice songs that match their skill levels. Additionally, the application may present song options in a "skill tree" format, visually illustrating skill progression and encouraging exploration of various techniques. A caching mechanism will provide quick access to user playlists, enhancing the overall user experience and making learning convenient and enjoyable.

## Contents
- [Kanban Board](https://github.com/orgs/spe-uob/projects/199)
- [Milestones](https://github.com/spe-uob/2024-PlaylistGuitarLessons/milestones)
- [Issues](https://github.com/spe-uob/2024-PlaylistGuitarLessons/issues)
- [Pull Requests](https://github.com/spe-uob/2024-PlaylistGuitarLessons/pulls)

## Stakeholders

- Client. Our client wants this software for his own personal use, so above all else it must fit his needs
- Us. We will fail our degree if we don't do this well, so we need to knock it out of the park. We also might use the software ourselves, so we want it to be fun to use
- Authors of guitar tabs/chords we scrape from the internet. Our app is based around scraping the web for other people's creations, so we must ensure we take our materials from places we have the right to access
- Spotify/other media companies. We will be connecting users' spotify accounts to our app (and potentially other music services), so we have to make sure we abide by their terms of service asnd don't do anything that could compromise their operation
- Guitarists writ large. We are making this app for guitarists who already have some experience with the guitar. As such, we mustn't bombard them with basic information, but instead should let them forge through at their level, providing resources for when they want to push past what they can currently do.
- Guitar Teachers. A tool like this will be invaluable to guitar teachers. It will both allow them to collate educational materials for their students, and encourage their students to keep playing in their own time.
  
## User Stories

As a beginner guitar player, I want to filter low difficulty songs tabs/chords, so that I can find songs that I can play at my current level, and continue with songs that I can play as I improve.

As a guitar teacher, I want to give my students a system where they can upload their own songs/playlists and get their tabs, so that my students can engage more with their learning.

As an intermediate guitar player, I want a way to filter song tabs by skills used, so that I can improve whatever skill I want to target.

As a guitar player who can't afford a teacher, I want a system with sections for difficulty of song tabs/chords, so that it can walk me through a useful learning journey.

## Bare Minimum Features
- Takes a list of songs and sends them to web scraper
- Scrapes web to return list of chords/tabs
- An algorithm to order tabs by difficulty
- A frontend that can present said information
- Some level of account integration
- Local hosting

## Key Features
- Takes song input from a Spotify playlist (including possibly spotify authentication)
- Can take input from a text box containing a list of songs
- Presents songs not as a list but as a 'skill tree', with branching paths based on different techniques
- A more visually appealing frontend
- A backend that caches user playlists for quick access next time
- Cloud hosting

## Bonus Features
- Songs appear multiple times in a tree at different difficulties
- Support for multiple playlists tied to one account
- Filtering songs by popularity (or other metrics)
- Integration of a tuner from elsewhere
- Interoperability for other music services (apple music, tidal, etc)
- Some level of recommendation for new songs
- Duolingo style streak
- Some level of teaching (feedback on playing, links to learning resources, etc)
- Mobile Support

## Software Modules (Services)
These are the five modules we think we will segment the software into. We will each take one area
- Music service interaction 
- Web crawler
- Ordering and classification of tabs
- Database, caching and account interaction (backend)
- Front end presentation

## Technology
- [React](https://react.dev/learn) for front end, with [TypeScript](https://www.typescriptlang.org/docs/) and [Vite](https://vite.dev/guide/)
- TypeScript for back end using [Nest.js](https://docs.nestjs.com/first-steps)
- [Spotify API](https://developer.spotify.com/documentation/web-api)
- [Prisma](https://www.prisma.io/docs) as an ORM with [PostgreSQL](https://www.postgresql.org/docs/) as the database

Architecture Diagram:

![arch_diagram](https://github.com/user-attachments/assets/7d04e9b5-88ef-4119-af8b-e12b0cfe0c17)

## User Instructions

So, here's how you use playlist guitar lessons:

1. Visit the website
2. log in with your spotify
3. pick a playlist
4. wait for the crawler to do its magic
5. check out the skill tree
6. click on a song and start playing!

   Your playlists will be saved to your account, so you can keep coming back to your skill tree as you develop your skills. Happy strumming!

## Developer Instructions
Greetings, ye who come after us. Find below all the information you could possibly need to continue development of this app.

### Contents
1. [Prerequisites](#prerequisites)
2. [Installation](#installation)
3. [Running the Development Server](#running-the-development-server)
4. [Folder Structure](#folder-structure)
5. [Development Notes](#development-notes)

### Prerequisites
Before you begin, make sure you have the following installed:
- npm (v6 or later)
- A code editor such as Visual Studio Code (which is what we used)
- Node.js (v14 or later)
- Package Manager: While npm works by default, you can use Yarn if preferred.

### Installation

1. Clone the Git Repo by running the following command in your local terminal:

Using SSH 

```git clone git@github.com:spe-uob/2024-PlaylistGuitarLessons.git ```

``` cd 2024-PlaylistGuitarLessons ```
