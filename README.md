# Aigeon AI Twitter 241

## Project Description

Aigeon AI Twitter 241 is a Python-based server application designed to interact with Twitter data through a series of API endpoints. This application provides a suite of tools to retrieve various types of user-related data from Twitter, such as user information, tweets, media, and social connections. It leverages the `FastMCP` server framework to define and manage these tools efficiently.

## Features Overview

- **User Information Retrieval**: Fetch detailed information about Twitter users using their usernames or IDs.
- **Social Connections**: Access data about user followings, followers, and verified followers.
- **Content Access**: Retrieve user tweets, replies, and media content.
- **API Versioning**: Supports multiple versions of certain API endpoints for enhanced flexibility.

## Main Features and Functionality

1. **Get User by Username**: Retrieve detailed information about a Twitter user using their username.
2. **Get Users by IDs**: Fetch information about multiple users using their unique Twitter IDs.
3. **Get User Replies**: Access replies made by a user, with support for pagination through cursors.
4. **Get User Media**: Retrieve media content posted by a user.
5. **Get User Tweets**: Access the tweets posted by a user, with pagination support.
6. **Get User Followings and Followers**: Obtain lists of users that a specific user is following or being followed by, including verified followers.
7. **API Versioning**: Some endpoints have multiple versions to accommodate different data retrieval needs.

## Main Functions Description

- **`get_user_by_username(username: str) -> dict`**: 
  - Fetches user information based on the provided username.
  - Returns a dictionary containing user details.

- **`get_users_by_ids(users: str) -> dict`**: 
  - Retrieves information for multiple users identified by their IDs.
  - Returns a dictionary with user data.

- **`get_users_by_ids_v2(users: str) -> dict`**: 
  - An alternative version of the `get_users_by_ids` function, potentially offering different data or performance characteristics.

- **`get_user_replies(user: str, count: str, cursor: str = None) -> dict`**: 
  - Retrieves replies made by a user, supporting pagination through a cursor parameter.
  - Returns a dictionary of replies.

- **`get_user_replies_v2(user: str, count: str, cursor: str = None) -> dict`**: 
  - An alternative version of the `get_user_replies` function, potentially offering different data or performance characteristics.

- **`get_user_media(user: str, count: str, cursor: str = None) -> dict`**: 
  - Fetches media content posted by a user, with pagination support.

- **`get_user_tweets(user: str, count: str, cursor: str = None) -> dict`**: 
  - Retrieves tweets from a user, supporting pagination through a cursor parameter.

- **`get_user_followings(user: str, count: str, cursor: str = None) -> dict`**: 
  - Obtains a list of users that a specific user is following, with pagination support.

- **`get_user_following_ids(username: str, count: str, cursor: str = None) -> dict`**: 
  - Fetches the IDs of users that a specific user is following, with a maximum count limit.

- **`get_user_followers(user: str, count: str, cursor: str = None) -> dict`**: 
  - Retrieves a list of followers for a specific user, with pagination support.

- **`get_user_verified_followers(user: str, count: str, cursor: str = None) -> dict`**: 
  - Fetches verified followers of a user, with pagination support.

This application is a powerful tool for accessing and managing Twitter data, providing developers with a robust framework for building Twitter-integrated applications.