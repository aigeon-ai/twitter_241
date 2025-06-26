# Aigeon AI Twitter 241

## Project Description

Aigeon AI Twitter 241 is a Python-based server application designed to interact with the Twitter API through the RapidAPI platform. This application provides a suite of tools to retrieve various types of user-related data from Twitter, such as user profiles, tweets, media, followers, and more. It leverages the FastMCP framework to create a set of tools that can be easily integrated into other applications or services.

## Features Overview

- Retrieve Twitter user information by username or user ID.
- Access user tweets, media, replies, and followings.
- Fetch user followers, including verified followers.
- Utilize versioned endpoints for enhanced data retrieval.
- Seamless integration with RapidAPI for API requests.

## Main Features and Functionality

The application offers a comprehensive set of features for interacting with Twitter data:

1. **User Information Retrieval**: Fetch detailed user profiles using either usernames or user IDs.
2. **User Content Access**: Obtain user tweets, media, and replies, with support for pagination through cursor-based navigation.
3. **Followings and Followers**: Retrieve lists of user followings and followers, including the ability to filter for verified followers.
4. **Versioned Endpoints**: Access different versions of endpoints to ensure compatibility and feature availability.

## API Endpoints or Main Functions Description

The application defines several key functions, each corresponding to a specific API endpoint:

- `get_user_by_username(username: str) -> dict`: Retrieves user information based on the provided username.
- `get_users_by_ids(users: str) -> dict`: Fetches user details for a list of user IDs.
- `get_users_by_ids_v2(users: str) -> dict`: An alternative version for fetching user details by IDs.
- `get_user_replies(user: str, count: str, cursor: str = None) -> dict`: Obtains user replies, with optional pagination.
- `get_user_replies_v2(user: str, count: str, cursor: str = None) -> dict`: A versioned endpoint for fetching user replies.
- `get_user_media(user: str, count: str, cursor: str = None) -> dict`: Retrieves media content posted by a user.
- `get_user_tweets(user: str, count: str, cursor: str = None) -> dict`: Accesses tweets posted by a user.
- `get_user_followings(user: str, count: str, cursor: str = None) -> dict`: Lists the users followed by the specified user.
- `get_user_following_ids(username: str, count: str, cursor: str = None) -> dict`: Fetches the IDs of users followed by the specified username.
- `get_user_followers(user: str, count: str, cursor: str = None) -> dict`: Retrieves followers of a user.
- `get_user_verified_followers(user: str, count: str, cursor: str = None) -> dict`: Lists verified followers of a user.

Each function makes an HTTP GET request to the corresponding endpoint on the RapidAPI platform, using a predefined set of headers for authentication.

## Configuration Parameters Explanation

The application uses the following configuration parameters:

- **RapidAPI Host**: `x-rapidapi-host` is set to `twitter241.p.rapidapi.com`, specifying the host for API requests.
- **RapidAPI Key**: `x-rapidapi-key` is a placeholder for the API key required to authenticate requests. This key should be replaced with a valid key obtained from RapidAPI.
- **Cursor**: An optional parameter used for pagination in endpoints that support it, allowing for efficient data retrieval in chunks.
- **Count**: Specifies the number of items to retrieve per request, with certain endpoints having a maximum limit (e.g., 5000 for following IDs).

This application is designed to be a robust tool for developers looking to integrate Twitter data into their applications, providing a flexible and efficient way to access a wide range of user-related information.