# Video Formatter UI

A single-page browser front end for the `video_formatter` API. You pick an Excel file of Google Drive video links, upload it, and the page saves the returned zip of formatted videos.

## Features

- File picker and upload button that posts the Excel file to `http://localhost:8000/process_excel/`
- Status messages while the job runs and when it fails, including the API's error text
- Streams the zip response straight to disk as `formatted_videos.zip` with StreamSaver.js, so large downloads are not held in memory

## Built with

- Plain HTML, CSS and JavaScript in one `index.html`
- [StreamSaver.js](https://github.com/jimmywarting/StreamSaver.js) 2.0.6, loaded from jsDelivr

## Run it

1. Start the `video_formatter` API on port 8000.
2. Open `index.html` in a browser, or serve the folder with any static file server, for example `python3 -m http.server`.
