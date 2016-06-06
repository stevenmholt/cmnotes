#Updated process for populating address information for a new location

###What?

We changed the process for populating the Address Details when a user creates a New Location.

###Why?

To make the User Experience easier and more in-line with the way the majority of situations play out.  As we watched how users create Locations, we found that upwards of 80% of the time, a Location winds up having the exact same Address Details as the Customer's Billing Details.

That means that 8 times out of 10, the user would have to click the "Use Billing Details" button which can get old after a while.

We also had users experience an issue when the Customer's Billing Details were in a country other than "United States" where the correct Country and State/Province would not be selected upon clicking "Use Billing Details".

This led us to re-examine the process and deliver a solution that fixes edge-case issues while also making life easier on the rest of the users.

#####Here's the setup

We have a Customer:
```
- First Name: Aaron
- Last Name: Aaronson
- Billing Information
--- Billing Name: Aaron Aaronson
--- Street Address: 1234 5th Street
--- City: Austin
--- Country: United States
--- State/Province: Texas
--- Postal Code: 73301
```

And we are going to create a Location for this Customer that just so happens to be at the same address the Customer uses for his Billing Information
```
- Location Name: Aaronson Home
- Type: Residential
- Street Address: _1234 5th Street_
- City: _Austin_
- Country: _United States_
- State/Province: _Texas_
- Postal Code: _73301_
```

**How it worked before**

When we pulled up the Aaron Aaronson customer and clicked "New Location"
Since we're wanting to create a Location that is the same as our Customer's Billing Details, we would have to click the "Use Billing Details" button to get the Street Address, City, Country, State/Provicne, and Postal Code populated correctly.

![alt text](https://github.com/stevenmholt/cmnotes/blob/master/images/NewLocation-PopDet-Before.png "New Location Before")

**How it works after**

Now when we pull up the Aaron Aaronson Customer and click "New Location", we see that there is a checkbox for "Same as customer's billing details" and it is already checked!

All we have left to do now is enter a Location Name, select the Type of location, and enter a Contact Name and Contact Phone Number then click "Save Location"

![alt text](https://github.com/stevenmholt/cmnotes/blob/master/images/NewLocation-PopDet-After-Check.png "New Location After, Check")
