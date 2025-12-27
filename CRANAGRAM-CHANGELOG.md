<div class="team-home">
  <a href="/team-waffles/">⬅️ Team Home</a>
</div>


![Cranagram](cranagram-banner.png)

<div style="
  background-color:#2c2f33;
  padding: 12px;
  display:flex;
  justify-content:center;
  gap: 30px;
  border-radius: 8px;
  margin-bottom: 20px;
">

  <a href="cranagram.html" style="color:white; text-decoration:none; font-weight:bold; font-family:Arial, sans-serif;">🏠 Cranagram Home</a>
  <a href="cranagram-privacy.html" style="color:white; text-decoration:none; font-weight:bold; font-family:Arial, sans-serif;">📜 Privacy Policy</a>
  <a href="cranagram-tos.html" style="color:white; text-decoration:none; font-weight:bold; font-family:Arial, sans-serif;">⚖️ Terms of Service</a>
  <a href="cranagram-version.html" style="color:white; text-decoration:none; font-weight:bold; font-family:Arial, sans-serif;">Version History</a>


</div>


# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.5.3-Beta] - 2025-12-27

### Added
- `/api/status` endpoint to check if user has already solved a puzzle globally (across all guilds)
- Global solve status checking - prevents duplicate solves across different Discord guilds
- "Already solved" UI state that displays previous solution word, time, and attempts
- Auto-hide Play button when puzzle is already completed

### Fixed
- Fixed bug where Play button incorrectly showed in other guilds after solving globally
- Improved solve status detection to work across all guilds, not just current guild

### Changed
- Enhanced solve status check to query globally (any guild) instead of per-guild only
- Improved user experience when switching between guilds after solving

---

## [0.5.2-Beta] - 2025-08-25

### Added
- Enhanced error handling for API failures
- Improved guess submission reliability
- Better user feedback messages

### Changed
- Code cleanup and refactoring
- Improved server stability

### Fixed
- Minor bug fixes and stability improvements

---

## [0.5.1] - 2025-08-25

### Added
- Solution word tracking in database (`solution_word` column)
- Solution word display in "already solved" UI
- Solution word included in score submission payload

### Changed
- Database schema migration: Added `solution_word TEXT` column via ALTER TABLE
- Score submission now includes the correct solution word for record-keeping
- Leaderboard data structure enhanced to support solution word retrieval

---

## [0.5.0] - 2025-08-25

### Added
- Reset countdown timer showing time until next puzzle (12-hour intervals at UTC noon/midnight)
- Auto-reload functionality when puzzle resets
- Display name support (`display_name` column) - shows Discord global names
- Avatar hash tracking (`avatar_hash` column) for user avatars in leaderboard
- Enhanced leaderboard with user avatars and display names
- Avatar URL generation for Discord CDN
- Improved leaderboard ordering: time-based priority (fastest solves first)
- Responsive layout system for mobile and desktop views
- Media query support for screen width < 980px

### Changed
- Database schema migration: Added `display_name TEXT` and `avatar_hash TEXT` columns
- Leaderboard now uses display names (global_name) with username fallback
- Leaderboard sorting improved: prioritizes completion time, then score, then attempts
- Server refactored from basic proxyserv to full-featured server implementation
- Enhanced score submission to include display name and avatar hash
- Better error handling with try-catch blocks and detailed error messages

### Fixed
- Leaderboard avatar display issues
- User identification consistency across guilds

---

## [0.4.0] - 2025-08-25

### Added
- Guess history system with localStorage persistence
- Per-puzzle guess tracking (stored with puzzle ID key)
- Visual guess list display with correct/incorrect indicators
- Guess count display
- Clear guesses functionality
- Guess deduplication (prevents counting same guess twice)
- Retroactive marking of correct guesses in history
- Maximum 100 guesses shown per puzzle
- Color-coded guess display (green for correct, gray for incorrect)

### Changed
- Improved guess submission flow with history integration
- Enhanced UI with guess history section
- Better state management for guess tracking

### Fixed
- Duplicate guess counting issues
- Guess history persistence across page reloads

---

## [0.3.0] - 2025-08-25

### Added
- Timer system with millisecond precision
- Timer display in MM:SS.D format
- Timer starts when Play button is clicked
- Timer stops when puzzle is solved
- Timer tracking in score submission (`timeMs`)
- Side timer display in responsive layout
- Attempt counter tracking unique guesses only
- Score calculation formula: `100 - 15 * (attempts - 1)`, minimum 10 points
- Input validation for 5-letter words only
- Form submission prevention during pending requests
- UI locking mechanism (`isSubmitting` flag) to prevent duplicate submissions
- Enter key prevention during submission

### Changed
- Enhanced guess submission with timing data
- Improved user feedback with timer display
- Better form handling with disabled states

### Fixed
- Race conditions in guess submission
- Multiple rapid submissions issue
- Timer accuracy and display

---

## [0.2.0] - 2025-08-25

### Added
- Per-guild leaderboard system
- SQLite database for score storage
- Score submission endpoint (`POST /api/score`)
- Leaderboard retrieval endpoint (`GET /api/leaderboard`)
- Database schema with guild_id, user_id, puzzle_id unique constraint
- Score, attempts, solved status, and timestamp tracking
- Leaderboard limit of 50 entries per puzzle per guild
- Basic leaderboard display in sidebar
- Score persistence across sessions

### Changed
- Enhanced from basic game to include competitive scoring
- Added database layer for persistent storage

### Fixed
- Score calculation and storage
- Leaderboard data retrieval

---

## [0.1.0] - 2025-08-24

### Added
- Initial Discord Activity integration
- Discord Embedded App SDK setup
- OAuth token exchange endpoint (`POST /api/token`)
- Discord authentication flow
- Basic Cranagram game functionality
- Puzzle fetching from cranagram.com API (`GET /cran/puzzle`)
- Guess verification via cranagram.com API (`POST /cran/guess`)
- Basic UI with rules screen and play area
- Letter display for jumbled words
- Guess input form
- Success/error message display
- Discord activity status updates
- Vite development setup
- Express server setup
- Basic error handling
- Project structure and configuration files

### Technical Details
- Client: Vite + vanilla JavaScript
- Server: Express.js with Node.js
- Database: SQLite (better-sqlite3)
- Authentication: Discord OAuth2
- API Integration: cranagram.com REST API


