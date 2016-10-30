# Registration

# Create Device Type

1. Click on Devices tab
2. Click on Add Device button
3. Click on Create Device Type 
4. Specify a Name and a Description
   - __Name:__ TiliIntelEdison
   > The device type name is used to identify the device type uniquely, using a restricted set of characters to make it suitable for API use.
   - __Description:__ Intel Edison IBM Watson Demo
   > The device type description can be used for a more descriptive way of identifying the device type.
5. Define a template
   > Define Template
   
   > > Use the options below to select attributes for the device type. All of these attributes are optional. They will be used as a template for new devices that are assigned this device type. Attributes you do not define may still be edited individually on devices that are assigned this device type.
   > > - Serial Number 
   > > - Manufacturer 
   > > - Model 
   > > - Class 
   > > - Description 
   > > - Firmware Version 
   > > - Hardware Version 
   > > - Descriptive Location 
   
   > Submit Information. You did not select any fields in the Define Template step. It is not mandatory to do so, but if you wish to define attributes that will act as a template for new devices that are assigned this device type, you may go back to that step and revise your decision - the fields you select will then appear here.
6. Metadata

# Add Device

1. Choose Device Type
   -  TiliIntelEdison
2. Device Info
   - > Device ID is the only required information, however other fields are populated according to the attributes set in the selected device type. These values can be overridden, and attributes not set in the device type can be added.
   - __Device ID__: TiliIntelEdisonDemo
   - Enter device ID (required)
3. Metadata (optional) 
   - > Metadata must be added as JSON; plain text cannot be used.
4. Security
   - You have two options:
   - > __Auto-generated authentication token.__ Allow the service to generate an authentication token for you. The token will be 18 characters long and will contain a mix of alphanumeric characters and symbols. The token will be returned to you at the end of the registration process.
   - > __Self-provided authentication token.__ Provide your own authentication token for this device. The token must be between 8 and 36 characters long, and should contain a mix of lower and upper case letters, numbers, and symbols (hyphen, underscore, exclamation-point, ampersand, at sign, question mark, period, right and left parentheses are permitted). The token should be free of repetition, dictionary words, user names, and other predefined sequences.
   - Provide a token (optional): Enter authentication token here
   - > Authentication tokens are encrypted before we store them. We are not able to recover lost authentication tokens. Ensure you make a note of the authentication token after clicking Add.
5. Summary
   - Please check that all submitted information for this device is correct before adding this device.
     - Device TypeTiliIntelEdison
     - Device IDTiliIntelEdisonDemo
     - Serial Number
     - Manufacturer
     - Model
     - Class
     - Description
     - Firmware Version
     - Hardware Version
     - Descriptive Location
     - Authentication Token
     - To be generated
     - Metadata
