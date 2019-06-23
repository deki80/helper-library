# helper-library
JavaScript library for common tasks

# class Validator
import class first: import Validator from 'Validator'

use static method validate to validate input fields:

Validator.validate(name, value, compareTo)

@param name - is equal to name attribute from html form

@param value - is value of input field

@compareTo - is used in cases where value should be the same as other input field, for example password and repeat password input fields.
If not provided, default value is set to false, and wont be use in validating.

Function returns an object with two properties: 
    {
        validated: Boolean
        error: String
    }

Error property will be either empty string if field is passed validation, or an string with error message.

- Could be added a functionality for better customising validation conditions, and response object...



