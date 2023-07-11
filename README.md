# PhoneNumberLocation
<!--Remove the below lines and add yours -->
The script is mainly use to find the Phone Number details in different ways:It Prints
1.Country code
2.Timezone
3.SIM Card Network name
4.Country Name

import phonenumbers : This line imports the phonenumbers module, which provides functions and classes to parse, format, and validate phone numbers.

from phonenumbers import timezone,geocoder,carrier :
This line imports some submodules from the phonenumbers module, which provide functions and classes to get the time zone, country, and carrier of a phone number.

number=input("Enter Your Number with +__:") :
This line prompts the user to enter a phone number with the country code prefix (such as +91 for India) and assigns it to the variable number.

phone=phonenumbers.parse(number) :
This line parses the input number into a PhoneNumber object, which stores the country code, national number, extension, and other attributes of the phone number.

time=timezone.time_zones_for_number(phone) : 
This line returns a list of time zone names for the given phone number object, such as [‘Asia/Kolkata’] for an Indian number.

carr=carrier.name_for_number(phone,"en") : 
This line returns the name of the carrier for the given phone number object and language code, such as ‘Airtel’ for an Indian number.

geo=geocoder.description_for_number(phone,"en") :
This line returns the geographic description for the given phone number object and language code, such as ‘India’ for an Indian number.

print(phone) : This line prints the phone number object in a standard format, such as +91 1234567890.
print(time) : This line prints the list of time zone names for the phone number object, such as [‘Asia/Kolkata’].
print(carr) : This line prints the name of the carrier for the phone number object, such as ‘Airtel’.
print(geo) : This line prints the geographic description for the phone number object, such as ‘India’.

## How to run the script
<!--Remove the below lines and add yours -->
Running the script is really simple! Just open a terminal in the folder where your script is located and run the following command :

    python Phone_Number.py


## Sample use of the script
<!--Remove the below lines and add yours -->
```
$ python Phone_Number.py 
   Enter Your Number with +__:+91 9876543210
    Country Code: 91 National Number: 9876543210
    ('Asia/Calcutta',)
    Airtel
    India
```
