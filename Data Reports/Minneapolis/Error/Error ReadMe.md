### Current Minneapolis Rental Report Data Error Log:

For the Minneapolis Rental Housing Report, I have used two open datasets from Minneapolis open data portal [Active Rental Licenses](https://opendata.minneapolismn.gov/datasets/cityoflakes::active-rental-licenses/about) and  [Assessors Parcel Data 2021](https://opendata.minneapolismn.gov/datasets/assessors-parcel-data-2021/explore). 

I have found errors on the datatable including the tax identification number (TID or apn). I encourage appropiate government officials to look at the respective tables and correct them in your database. **High quality clean data is important for accuracy and reduce conflicts for internal reporting**

**Please feel free to email me at anayeem1@gmail.com if you questions**


1) Issue: On the Active Rental Licenses Dataset, there are license entries of expired rental leases. Are they no longer active?
* Last Report Made: March 1st, 2022 
* [Retired Licenses Entry](https://github.com/PreLease/community-data-reports/blob/e72558e55b1632ef192cccdf57d24c918625859c/Data%20Reports/Minneapolis/Error/Rental_ExpiredEntries.csv)
* Entry Impact: 384
* Request: Is there a reason why the information is there and should it be excluded?

2) Issue: On the Active Rental Licenses Dataset, there are some licenses with the same TID, which is suppose to be unique
* Last Report Made: March 1st, 2022 
* [Multiple TID Data](https://github.com/PreLease/community-data-reports/blob/e72558e55b1632ef192cccdf57d24c918625859c/Data%20Reports/Minneapolis/Error/Rental_MultTID_Entries.csv)
* Entry Impact: 752
* Request: Is there a reason for this, if not correct accordingly 

3) Issue: On the Active Rental Licenses Dataset, there are TIDs that have letters, which seems out of place
* Last Report Made: March 1st, 2022 
* [TIDs with Letters Data](https://github.com/PreLease/community-data-reports/blob/e72558e55b1632ef192cccdf57d24c918625859c/Data%20Reports/Minneapolis/Error/Rental_TID_A_Entries.csv)
* Entry Impact: 15
* Request: Remove them?

4) Issue: When merging both datasets, here are the rental licenses that did not have match with the Assessor's dataset
* Last Report Made: March 1st, 2022 
* [Active Rental TIDs without matching Assessor Data](https://github.com/PreLease/community-data-reports/blob/e72558e55b1632ef192cccdf57d24c918625859c/Data%20Reports/Minneapolis/Error/Single_TID_Non-Match_Entries.csv)
* Entry Impact: 141
* Request: The active rental license dataset may include new properties that are assessed yet, or it could just be missing.

5) Issue: When merging both datasets, I've noticed that the ACTUAL TID is suppose to be different in Active Rental License dataset
* Last Report Made: March 1st, 2022 
* [Incorrect TIDs between the two datasets](https://github.com/PreLease/community-data-reports/blob/e72558e55b1632ef192cccdf57d24c918625859c/Data%20Reports/Minneapolis/Error/Incorrect_TIDx_Entries.csv) 
* COMMENT: The TID_x is the TID from the assessor data, while the TID_y is from Active Rental Licenses. Notice multiple TIDs
* Entry Impact: 194
* Request: Why did error occur? Should the TID for Active Rental licenses be updated

6) General Issues: On the Active Rental Licenses Dataset, there are some missing geo-coordinates, and community desginations

7) Inconsistent Values on people's Identity: Is there a way to uniquely identify owners regardless if they misspell their name. 

