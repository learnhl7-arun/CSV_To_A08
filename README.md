# CSV_To_A08
This Channel takes a CSV File as input and transforms it into an A08 Messages. For each line in CSV File, a seperate .hl7 file is created. 

The first line of the CSV File is expected to be the header. 
Structure of CSV File is 
Number,Gender,NameSet,Title,GivenName,MiddleInitial,Surname,StreetAddress,City,State,StateFull,ZipCode,Country,CountryFull,EmailAddress,Username,Password,BrowserUserAgent,TelephoneNumber,TelephoneCountryCode,MothersMaiden,Birthday,Age,TropicalZodiac,CCType,CCNumber,CVV2,CCExpires,NationalID,UPS,WesternUnionMTCN,MoneyGramMTCN,Color,Occupation,Company,Vehicle,Domain,BloodType,Pounds,Kilograms,FeetInches,Centimeters,GUID,Latitude,Longitude

Following is CSV field to ADT Message Mapping 

CSV_#	CSV_Field	      HL7_2.8-Field
------  -----------   ------------
CSV_1   Number	       PID-3.1
CSV_4   Title	         PID-5.5
CSV_5   GivenName	     PID-5.2
CSV_6   MiddleInitial  PID-5.3
CSV_7   Surname	       PID-5.1
CSV_8   StreetAddress  PID-11.1
CSV_9   City           PID-11.3
CSV_11  StateFull	     PID-11.4
CSV_12  ZipCode        PID-11.5
CSV_13  Country	       PID-11.6
CSV_21  MothersMaiden  PID-6.2
CSV_22  Birthday       PID-7
CSV_29  NationalID     PID-3.1

Instructions to use the channel
-------------------------------
1. Import /code/CSV To HL7 ADT A08.xml into Mirth Connect
2. In Source Tab change 
   a. Director
   b. Move-to-Directory
   c. Error Move-to- Directory
3. In Destinations Tab change
   a. Directory


