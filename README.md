# GoLangProjectSteps

This readme aims to provide practical steps towards learning GoLang. The repo is intentionally empty other than this README file.

## Step 1

Create a new Go project. Use the latest version of Go.
Build it and run it, it should print "Hello World"

## Step 2

Create a new endpoint on `/status`. It should always return a 200 Success status and a message indicating the endpoint is working

## Step 3

Add a new POST endpoint on `/username`. It should parse a username out of the request body, and print the username in the response. The request should have a `key : value` structure. e.g. 
```json    
{
    "username" : "MarcMurphy"
}
```

The structure of the request body is up to you, it does not need to be JSON, as long as (in this case) `MarcMurphy` is returned.

If the endpoint is called as a non POST request, the request should be rejected with an appropriate error message and status code.

If the endpoint is called and there is no username provided, the request should be rejected with an appropriate error message and status code.

## Step 4

Store the username in memory. If a request is received and the username already exists, reject the request.

## Step 5

Persist the stored usernames after a server reboot. How this works is up entirely to you.

## Step 6

Create a new endpoint `/jwt`. It parse a `username` out of the request body, and return a valid JWT. Any extra parameters provided in the request body should be ignored.

## Step 7

Sign the JWT

## Step 8

Create a new endpoint `/auth` which accepts a JWT. If the request has been signed by our service, and contains a `username` that is stored in our service, return an appropriate JWT.