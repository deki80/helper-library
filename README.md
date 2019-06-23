# helper-library
JavaScript library for common tasks

# class Validator
import class first: import Validator from 'Validator'

use static method validate to validate input fields:

Validator.validate(name, value, compareTo)

@param name - is equal to name attribute from html form

@param value - is value of input field

@compareTo - is used in cases where value should be the same as other input field, for example password and repeat password input fields.
If not provided, default value is set to false, and won't be used in validating.

Function returns an object with two properties: 
    {
        validated: Boolean,
        error: String
    }

Error property will be either empty string if field is passed validation, or an string with error message.

- Could be added a functionality for better customising validation conditions, and response object...

#postRequest
- use case:
import postData from 'postRequest'

@param url - API url to post data (String),
@data - data to be send (Object).

example:

const url = 'someapi.com/api/post'
const data = {name, password, email}

postData(url, data)

- function has two additional params @contentType and @auth
default value for @contentType is 'json' and default value for @auth is false

if post request should be authenticated, auth token should be provided as fourth param

- Should refactor content type option for better handling multipart/form-data


