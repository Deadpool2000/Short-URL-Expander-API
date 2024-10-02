# Short URL Expander API

The **Short URL Expander API** allows you to expand shortened URLs and follow all possible redirections. This API is useful when you want to trace the final destination of a shortened URL.

## Features

- Expand shortened URLs
- Follow all possible redirections
- Get the final destination URL

## API Endpoints

### `GET /extract`

Expands a shortened URL by following all redirections until the final destination URL is reached.

#### Request

- **URL**: `/extract`
- **Method**: `GET`


#### Body Parameters:

| Parameter | Type   | Description                        | Required |
|-----------|--------|------------------------------------|----------|
| `url`     | string | The shortened URL to be expanded   | Yes      |

Example (Local Testing):

```
https://127.0.0.1:5000/extract?url=https://bit.ly/example
```

