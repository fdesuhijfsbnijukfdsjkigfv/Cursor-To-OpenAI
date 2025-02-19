# Cursor To OpenAI

Convert the Cursor editor into an OpenAI-compatible API service.

## Project Overview

This project provides a proxy service that transforms the AI capabilities of the Cursor editor into an OpenAI-compatible API, allowing you to reuse Cursor's AI features in other applications.
- Supports multiple cookies at the same time, separated by commas.

## Prerequisites

1. Visit [www.cursor.com](https://www.cursor.com) and complete the registration and login process (you get 150 free quick responses, which can be reset by deleting your account and re-registering).
2. Open the developer tools in your browser (F12).
3. Locate the `WorkosCursorSessionToken` value in **Application → Cookies** and save it (this is equivalent to an OpenAI API key).

## API Documentation

### Basic Configuration

- **API Endpoint:** `http://localhost:3010/v1/chat/completions`
- **Request Method:** `POST`
- **Authentication:** Bearer Token (use the value of `WorkosCursorSessionToken`, supports multiple keys separated by commas)

### Request and Response Format

The request and response formats follow OpenAI's API standards.

## Deployment and Usage

### Docker Deployment

```sh
docker run -d --name cursor-to-openai -p 3010:3010 ghcr.io/jiuz-chn/cursor-to-openai:latest
```

### Local Development

```sh
cd Cursor-To-OpenAI
npm install
npm run start
```

## Important Notes

- Keep your `WorkosCursorSessionToken` secure and do not share it with others.
- This project is for educational and research purposes only. Please comply with Cursor's terms of use.

## Acknowledgments

- This project is optimized based on [cursor-api](https://github.com/zhx47/cursor-api) (by zhx47).
- It also integrates improvements from [cursor-api](https://github.com/lvguanjun/cursor-api) (by lvguanjun).
