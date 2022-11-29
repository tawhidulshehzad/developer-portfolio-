# Used Products Resale Market

Your website has to be related to selling used (second-hand products) with the ability to advertise a product.Some examples are **Buy-sell** second-hand furniture, car, bike, truck, bus, books, cooking utensils, mobile phones, headphones, laptops, laptop parts, watches, TV, exercise equipment, camera, clothes, music instruments, Fridge, A/C, etc. Remember, you will have to **choose only one types of product**. For instance, if you select furniture, then you **cannot** sell any other products, such as mobile phones, instruments, etc., other than furniture.

1. **IMPORTANT:** Make sure your design is **unique**. Your code and design must not match any of the **projects implemented in our course**. You must not copy your **previous assignments** or any **practice project** displayed in the course or in our **conceptual sessions**. Failing to satisfy any of the above conditions will cost you a significant mark or even 0.

3. Take your time thinking about the design. Just spend 30 minutes or an hour and then start your project. If needed, put a placeholder image and work on developing the functionalities. Once you are done, replace them with relevant images.

4. Use the Environment variable on both the client (firebase config) and server side (MongoDB credentials, Access token secret, stripe, etc.). Use the .gitignore file on the server side.

5. It is important to note that your UX design should be good. For example, suppose a user does not see data when they visit a route, does not see the ad after posting the advertisement without reloading the site, or gets logged out when visiting a private route right after signing up. In that case, etc., then **you may lose a significant mark for that**.

## Main Requirements

1. Your homepage will have a **navbar** , a banner/slider, Advertised items, second-hand **product categories** section and a realistic **footer**. Your navbar will have a **login** button. Implement email/password-based authentication and at least one social login(google, Facebook, GitHub, etc.) authentication. **Create an extra field for options. There will be two options: a radio button, a dropdown, a toggle button, etc. If the user creates a seller account, he will choose the seller option. Otherwise, a normal user will have the user option selected by default**. Users logged in by using social media will be considered as buyers. 



3. **You will have to decide what would be the categories of the second-hand product you have selected.** For instance, if your website is about second-hand furniture, you can divide your categories into the bedroom, kitchen, dining room, etc.; if it is about second-hand car, your categories can be a Microbus, luxury car, electic car, etc. Or you can categorize second-hand products under brand names if you want. However, make sure it is relevant. You will need at least 3 categories, each with at least 2 products.

4. When the user clicks on a category on the home page, they will be redirected to the **/category/:id** route, where they will see **second-hand products under that category only**. The **/category/:id** page will have a column(s) of cards. It can be 1,2, or 3 columns. Each card will have a picture, name, location, resale price, original price, years of use, the time when it got posted, the seller's name; if the seller is verified, there will be a blue tick next to their name and a **Book now** button. Please note, category:/id will be a private route. 

5. On clicking the **Book now** button, a form in a modal will popup with the logged-in user name and email address, item name, and price(item name, price, and user information will not be editable) by default. You will give your phone number and meeting location, and lastly, there will be a submit button. After clicking the submit button, you will have to inform the buyer with a modal/toast that the item is booked.

6. 

      **Note:** Do not apply email verification as it will be an inconvenience for the examiner. It is important for the examiner to be able to check your authentication without any hassle. If you want, you can add email verification after getting the assignment result.

7. If a user(buyer/seller/admin) is logged in, they will see **logout** (should be working) and another option on the header called Dashboard. The dashboard routes will change based on the users:

      **Buyers will see:** My orders(see bonus requirement 7),

      **Sellers will see:** Add A product (See Requirement 8), My Products(see requirement 9), My buyers(this one is optional).

      **Admin will see:** All Sellers, All Buyers (see requirement 12), Reported Items



9. On the **"My Products"** page, display sales status (available or sold), price, and any other relevant information you want to show. A seller will be able to delete any of his/her product. Please note there will be a special button for each unsold/available product where the seller can hit the button to advertise. 

10. The advertised items will appear on the home page. Please note if there are no items marked as advertised, the advertised items section won't be displayed on the home page. The advertised section will only appear if there is one or more available (unsold items) are marked to be advertised.



12. In the **All Sellers,** the Admin will see the sellers. On the **All Buyers** route, the Admin can see all the Buyers. If the Admin wants, he can delete any buyers or sellers.

13. 





## Bonus Requirements

4. Implement an extra feature: **WishList** or **Report to Admin**(choose one) in the /category/:id route. A buyer can make a product to his/her wishlist or report an item by clicking a relevant button. If you have implemented the wishlist feature, show them in the buyer's Dashboard in a separate route, "My WishList." A user should be able to purchase the item from the wishlist page. (Just redirect the user to the purchase page)

   If you have implemented the "report to admin" feature, show the reported items in the admin dashboard in a separate route, "Reported Items" (tips: create a separate collection for the wish list and filter by user email address). An admin will be able to delete a reported item. 

5. Implement the basic version of the JWT token for email/password-based authentication. Upon social login, registration, and login, you will create a JWT token and store it on the client side. You will send the token for my orders, buyers, and advertisements routes and verify the user.

6. The **all-sellers** route will have a name, email address, delete button, and verify button. Admin will be able to verify a seller. When clicked on the verify button, the seller's status will change from unverified to verified(show a blue tick when the seller is verified), and this status will be shown on the products added by a verified seller.

7. The **My Orders** route will have a table/cards. Each card/ table row will be an order having an image, title, price, and a pay button. On clicking the pay button, to take the user the payment page with fields for card details will pop up, or the user will be taken to a route where there will be a form for filling up card details. Save the payment information in the database and inform the user via a modal/toast. Don't forget to update the button text to "paid" after payment. Please note, payment will be done by Stripe. 

      Once an item is paid, it won't be displayed on the advertised item or on the category page. Only available items will be displayed to be purchased.







### Optional

1. Explore [react-image-gallery](https://www.npmjs.com/package/react-image-gallery)and use a slider instead of a picture in your /advertisement/:id route
2. Add generic modal
3. Add a search bar on the homepage and show advertisements based on the search key
4. Add animation on the homepage
5. Add another route," **My Buyers,"** where you will have to show the Buyers name, email, item purchased, etc.
6. Create a Make Admin route for the admin. Here an admin (admin only) will be able to make any buyer or seller an admin.

### **What to submit**

1. Client-side code GitHub repository
2. Server-side code GitHub repository
3. Live website link
4. **IMPORTANT:** For the examiners to check your admin routes, create a user for your site, give the email address: admin role and add this user's credentials in the client side readme in this **exact format** :

adminEmail: \<your admin email\>

adminPassword: \<your admin password\>

Otherwise, you won't get any marks for your admin routes.
