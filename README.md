# Audio Playback Application Documentation

This documentation outlines the functionality and features of the Audio Playback Application, a web-based tool designed for uploading audio tracks, selecting specific parts of these tracks, arranging these parts on a common timeline, and playing them sequentially. The application also includes a visual playback indicator and supports drag-and-drop reordering.

## Installation
use 
```
npm i
npm start
```
to start the react applicaton on localhost:3000


## Features

- **Audio Track Upload**: Enables users to upload audio tracks for playback and manipulation.
- **Part Selection**: Allows users to select segments from uploaded tracks to add to a common timeline by clicking on the selected piece.
- **Sequential Playback**: Facilitates the sequential playback of selected audio parts on the common timeline, with a moving pointer to indicate the current playback position.
- **Drag-and-Drop Reordering**: Provides an interface for reordering audio parts on the timeline through drag-and-drop actions.

## Component Structure

### AudioTrack Component

Responsible for displaying individual audio tracks with functionalities to play, pause, and select parts of the track.

- **Props**:
  - `track`: Information about the track including its URL and selected parts.
  - `onSelectPart`: Callback function for handling part selection.

### CommonTimeline Component

Displays the selected audio parts on a shared timeline, supports sequential playback with visual indicators, and allows drag-and-drop reordering.

- **Props**:
  - `parts`: Array of selected audio parts.
  - `onDragEnd`: Callback function for handling the reordering of parts.

## Implementation Details

- **State Management**: Utilizes React's `useState` and `useRef` for managing component states and referencing DOM elements.
- **Audio Playback**: Employs the Web Audio API for precise audio playback control, including segment-specific playback.
- **Drag-and-Drop Functionality**: Integrates `react-beautiful-dnd` for an intuitive reordering interface.
- **Visual Playback Indicator**: Implements a dynamic pointer that moves across the timeline to indicate current playback position.
- **Interfaces usage**: Using the TrackPart interface to store the endTime and startTime along with the trackUrl to play the selected audio section on the common timeline, one by one.



## Conclusion

The Audio Playback Application showcases the potential of React and the Web Audio API in creating a comprehensive audio manipulation tool. It addresses key challenges in audio processing and user interface design, offering a robust platform for interactive audio engagement with ample room for further development and expansion.
