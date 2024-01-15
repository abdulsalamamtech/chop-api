**CHOP API DOC**

#1 *users*
id
name,
email,
phone_number
role
is_admin
status
updated_at
created_at

#2 *addresses*
id
street
city
lga
state
country
zip_code
status
updated_at
created_at

#3 *upload_images*
id
file_id
url
size
status
updated_at
created_at

#4 *upload_videos*
id
file_id
url
size
status
updated_at
created_at

#5 *categories*
id
name
slug
image_id
video_id
added_by //user_id or admin
status
updated_at
created_at

#6 *products*
id
name
slug
category_id
image_id
video_id
added_by //user_id or vendor
ingredents
available //yes or no
price
delivering_time
tags // vendor->name / category->name / product->name etc
status
updated_at
created_at

#7 *orders*
id
user_id
address_id
product_id
quantity //1-10
total_price
paid //yes or no or 1/0
status
updated_at
created_at

#8 *payments*
id
order_id
session_id
payment_provider //  paystack
payment_method = 
status
updated_at
created_at


id
name
status
updated_at
created_at
