# Short URL Expander API

The **Short URL Expander API** allows you to expand shortened URLs and follow all possible redirections. This API is useful when you want to trace the final destination of a shortened URL.

## Features

- Expand shortened URLs
- Follow all possible redirections
- Get the final destination URL

## Installation

    git clone https://github.com/Deadpool2000/Short-URL-Expander-API

    pip install flask

    cd Short-URL-Expander-API/

After this, just run code - 

    python3 app.py

    

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

## Example Output

This is an example short link - 

https://bit.ly/3Bg19uM

Expected output will be - 

```
{
  "All Possible Redirections": [
        "https://www.usatoday.com/story/travel/2022/02/10/amtrak-deal-valentines-offer-sale/6741296001/",
        "https://www.usatoday.com/story/travel/2022/02/10/amtrak-deal-valentines-offer-sale/6741296001/"
  ],

  "Full Link": "https://www.usatoday.com/story/travel/2022/02/10/amtrak-deal-valentines-offer-sale/6741296001/",

  "Original URL": "https://bit.ly/3Bg19uM"
}
```