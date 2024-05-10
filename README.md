Sure, here's the updated README:

---

# Video Player HLS POC

This project is a proof of concept (POC) for handling videos on the web using HLS (HTTP Live Streaming) and FFmpeg. It demonstrates how to convert a video into HLS format using FFmpeg and then stream it on a web player.

## Project Structure

The project is divided into two main parts:

1. **Backend Server** - This is a Node.js server that handles video upload, conversion to HLS format using FFmpeg, and serving the HLS files.

2. **Frontend Client** - This is a React application that uses Video.js to play the HLS video.

## Backend Server

The server is built using Express.js and uses the `multer` library for handling file uploads. The uploaded video file is then converted into HLS format using FFmpeg. The HLS files are stored in the `uploads` directory and served statically.

The server also uses CORS middleware to allow requests from the frontend client. To upload the video, you will need to use Postman or a similar tool to send a POST request to the server.

## Frontend Client

The client is a React application that uses Video.js for playing the HLS video. The Video.js player is initialized with the HLS video URL received from the server. This URL is obtained from the response of the POST request made to the server for video upload.

## How to Run

0. Remember you should have `ffmpeg` installed in your system before hand.
1. Clone the repository.
2. Install the dependencies using `npm install`.
3. Start the backend server using `node index.js`.
4. Start the frontend client using `npm start`.
5. Use Postman to upload a video to the backend server and obtain the HLS video URL.
6. Encode the obtained URL in the frontend client to start streaming the video.

## Dependencies

- Node.js
- Express.js
- Multer
- FFmpeg
- React
- Video.js
- Postman (for video upload)

## Limitations

This is a POC and not meant for production use. The server does not handle video conversion in a queue and does not scale for multiple concurrent uploads.

## Future Improvements

- Implement a queue for handling video conversion.
- Add error handling for video upload and conversion.
- Improve the UI of the video player.

---

## Detailed Blog and Documentation Used
[ChaiCode Video Streaming Tutorial](https://chaicode.com/blogs/full-stack-video-streaming-platform)

[CloudFlare- What is HLS: HTTP Live Streaming](https://www.cloudflare.com/learning/video/what-is-http-live-streaming/)