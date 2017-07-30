# UserCreation
GUI to create new users with templates or in batches

## Description

One task that every systems administrator has to go through at some point is the creation of new user accounts.  Over time, this becomes burdensome and tedious.  The Active Directory wizard takes you through multiple screens and you have to enter the same information multiple times in some occasions (e.g. a lot of organizations use FirstName.LastName for samAccountNames).  It also does not allow you to set all of the fields that you want included in the wizard.  I wanted a way to include those fields and an option to set defaults for some fields.  Luckily Powershell makes all of that possible in an easy to use way.  Powershell does all of the heavy lifting and an optional XML file saves even more time by pre-populating certain fields and setting defaults.  You also have the ability of bulk-adding users via CSV.  To create users from a CSV, click on File > CSV Mode.  You can then import the CSV and browse through the users in the CSV.  Once the CSV is imported, you can create one user at a time or all at once.  If you want a CSV template created for you, click on File > Create CSV Template.

## Features

* Allows user creation with oft-used Active Directory attributes
* Bulk creation of users from CSV
* Auto-generation of account attributes based on other attributes
  * Display Name
  * samAccountName
  * userPrincipalName
* Default entries
  * Domain
  * OU
  * Phone Number (can use full number or company prefix '212-555-')
  * Department
  * Company
  * Description
  * Password (Accounts are set to change at first logon)
  * Site (HQ, Branch Office 1, etc)
  * Street Address
  * City
  * State
  * Postal Code
* Pre-populated fields for easy selection
  * Address information
  * Domains
  * OUs
  * Descriptions
  * Departments

## Changelog

1.2 - 2012/12/04
* Added check for XML Options file - Will now prompt to create one if not found
* Added XML Options file version check
* Fixed bug where Display Name, sAMAccountName, and UPN were not being generated correctly for CSV files
* Title and Description should be set correctly when creating users from CSV

1.1 - 2012/05/13
* Added ability to select custom format for sAMAccountName, UPN, and Display Name
* Minor bug fixes

1.0 - 2012/03/03
* Updated to be compatible with PowerShell v3
* Enter custom sAMAccountName, Display Name, and userPrincipalName in single-user and CSV modes
* Turn off auto-generation of sAMAccountName, Display Name, and userPrincipalName in single-user mode
* Better error-handling during user creation
* Set new accounts as enabled or disabled
* Set 'Password must change at logon' to enabled or disabled 
* Minor bug fixes
