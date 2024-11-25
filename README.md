# Custom Video Player

This project is a responsive web application built as part of the course "JavaScript Web Projects: 20 Projects to Build Your Portfolio" by Zero To Mastery. The custom video player enhances user experience with features such as play/pause, volume control, progress tracking, playback speed adjustment, and fullscreen mode.

## Table of contents

- [Custom Video Player](#custom-video-player)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [Screenshot](#screenshot)
    - [Links](#links)
    - [Features](#features)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Useful resources](#useful-resources)
  - [Author](#author)
  - [Acknowledgments](#acknowledgments)

## Overview

This project includes the following features:
- A custom-designed video player with intuitive controls.
- Playback control with play, pause, and progress bar.
- Volume adjustment and mute/unmute functionality.
- Customizable playback speed.
- Fullscreen mode support for enhanced viewing.
- Responsive design ensuring optimal user experience on different screen sizes.

### Screenshot

![](./screenshot.png)

### Links

- Live Site URL: [DT Code](https://video-player.dtcode.se/)

### Features

- Play/Pause Controls: Click the button or the video itself to toggle playback.
- Volume Control: Adjust volume with a slider or mute/unmute using an icon.
- Progress Tracking: Visual progress bar for seeking and displaying elapsed time.
- Playback Speed Adjustment: Select different speeds from a dropdown menu.
- Fullscreen Mode: Enter and exit fullscreen seamlessly with a single button.
- Responsive Design: Adaptable to various screen sizes for mobile and desktop users.

### Built with

- HTML5: For semantic video elements and application structure.
- CSS3: For custom styling and responsive design.
  - CSS Variables for consistent theming.
  - Media Queries for mobile optimization.
- JavaScript (ES6+): For interactivity and functionality.
  - DOM manipulation for dynamic updates.
  - Event handling for user interactions.
  - Fullscreen API for toggling fullscreen mode.

### What I learned

In this project, I learned:
- How to enhance the default video player by adding custom controls using JavaScript.
- Managing video events (e.g., play, pause, timeupdate) to update the UI dynamically.
- Using the Fullscreen API to toggle fullscreen mode programmatically.
- Building responsive interfaces and intuitive UX for video controls.

Example code for updating the progress bar dynamically:

```js
function updateProgress() {
    progressBar.style.width = `${(video.currentTime / video.duration) * 100}%`;
    currentTime.textContent = `${displayTime(video.currentTime)} /`;
    duration.textContent = `${displayTime(video.duration)}`;
}

function displayTime(time) {
    const minutes = Math.floor(time / 60);
    let seconds = Math.floor(time % 60);
    seconds = seconds > 9 ? seconds : `0${seconds}`;
    return `${minutes}:${seconds}`;
}
```

### Useful resources

- [MDN Web Docs: HTMLMediaElement API](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement) - Detailed information about video and audio properties and methods.
- [MDN Web Docs: Fullscreen API](https://developer.mozilla.org/en-US/docs/Web/API/Fullscreen_API) - Helped with implementing fullscreen functionality.
- [Font Awesome](https://fontawesome.com/) - Used for icons like play, pause, and volume controls.

## Author

- GitHub - [@dantvi](https://github.com/dantvi)
- LinkedIn - [@danieltving](https://www.linkedin.com/in/danieltving/)

## Acknowledgments

Special thanks to Zero To Mastery for providing the guidance and course material for this project. This project significantly improved my understanding of video controls, event handling, and responsive design.
