**CHOP API DOC**

##About Chop
Chop is an 

##1 *users*
id
name,
email, (abdulsalamamtech@gmail.com)
phone_number (+2349091922467)
role (customer, vendor, rider, admin)
is_admin (1 / 0)
status
updated_at
created_at

##2 *addresses*
id
user_id
street
city
lga
state
country
zip_code
status
updated_at
created_at

##3 *user_info*
id
user_id (vendor / rider)
about
description
status
updated_at
created_at

##4 *upload_images*
id
file_id
url
size
status
updated_at
created_at

##5 *upload_videos*
id
file_id
url
size
status
updated_at
created_at

##6 *categories*
id
name
slug (full-name . rand_int(00-99))
upload_image_id (required)
upload_video_id (nullable)
admin_id (user_id / admin_id / added_by / Auth::user->id)
status
updated_at
created_at

##7 *products*
id
name
slug (full-name . rand_int(00-99))
category_id
upload_image_id (required)
upload_video_id (required)
vendor_id (user_id / vendor_id / added_by / Auth::user->id)
ingredients
available (yes / no)
price  (double 10.2)
delivering_time
tags (vendor->name / category->name / product->name etc)
status
updated_at
created_at

##8 *orders*
id
user_id (user_id / customer_id / added_by / Auth::user->id)
address_id
product_id
quantity (1-10)
total_price (double 10.2)
paid (yes / no or 1 / 0)
status
updated_at
created_at

##9 *payments*
id
order_id
session_id
payment_provider (paystack / flutterwave / interswitch)
payment_method = (card)
status
updated_at
created_at

##10 *deliveries*
id
order_id
payment_id
rider_id (user_id / rider_id / added_by / Auth::user->id)
approved_by_vendor (vendor 1 / 0)
approved_by_rider (rider 1 / 0)
approved_by_customer (user 1 / 0)
status
updated_at
created_at


## Registration
>> api/register?user=customer
>> api/register

>> api/register?user=vendor
>> api/register/vendor

>> api/register?user=rider
>> api/register/rider
