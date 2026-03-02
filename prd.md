## Develop Home Page (Search, Filter, Browse):

1. Display images/artworks/services dynamically fetched from the database.
2. Support search and filtering by category, vendor/photographer, or keyword.
3. Ensure responsive design across devices.
4. Include a functional navbar/header and footer.

## Vendor Gallery & Management

- Public-facing gallery for each vendor (photographer, artist, or stock contributor).
- Vendor-only management page to **upload, edit, or delete** images/artworks.
- Access control to ensure only vendors can manage their own gallery.

## Item Details Page

- Show detailed information: image, title, description, price, availability.
- Options to:
  - Add item(s) to the basket.
  - Book a session (for Photography Studio).
  - Select rental duration & delivery location (for Art Lease).
- Use **form validation** and provide feedback for invalid inputs.

## Checkout Page

- Display selected items with options to **add, update, or remove items**.
- Handle **empty basket** scenarios by preventing checkout if no items are selected, showing a clear message, and providing a **“clear basket” button**.
- Calculate and display **totals dynamically**.
- Collect user details, including **name, contact, and payment information**.
- Allow selection of **delivery or booking methods** (e.g., photography session booking, art lease with rental/delivery, stock image purchase).
- Show a complete **order summary with accurate totals** before final submission.
- Validate all form inputs and handle invalid data gracefully with clear feedback messages.
- Ensure the layout is **responsive, intuitive, and professionally styled**.

## Authentication and Access Controls

- Implement a complete user authentication system, including **Registration, Login,** and **Logout**, using hashed passwords and session-based authentication.
- Restrict admin access for managing all content, vendors, and orders.
- Restrict vendor access for managing personal gallery.
- Restrict customer access for browsing, booking, and purchasing. 
- Implement access control using **custom decorators** (e.g., `@admin_required`) or **Flask-Login session-based role checks**.
- Do not use **Flask-Admin**.

## Error Handling:

- Handle and display custom error pages for at least:
  - 404 Not Found.
  - 500 Internal Server Error.
- Use an error.html template.
- Flask `@app.errorhandler` should manage redirection and display.

## Professional User Interface:

- Your interface must:
  - Be responsive across screen sizes.
  - Have a consistent color scheme, fonts, and layout.
  - Avoid overlapping or broken elements.
  - On all pages, ensure that you include:
    - Navigation bar/header.
    - Page footer.
    - Error-free forms and buttons.
    - Clear spacing and alignment.

## Database Integration and Sample Data:

- Your application must be built on the **data model developed in Assessment 2**, with any necessary refinements to support full functionality.
- The database must include:
  - **At least 15 individual items in total** (e.g., photographs, artworks, or stock images), distributed across a minimum of **2 different item categories.** For example, "Wedding Photography" and "Event Photography" for a studio, "Paintings" and "Sculptures" for art lease, or "Nature" and "Architecture" for stock images would be two distinct categories.
  - At least 6 users, including:
    - **2 admin users** with full system privileges.
    - **2 vendor users** (e.g., photographers, artists, or stock contributors) responsible for managing their own gallery.
    - **2 customer users** who can browse, book, lease, or purchase items.
  - At least 3 completed transactions  (orders, bookings, or leases), each demonstrating a different purchase or booking method. Examples:
    - A photography session booking.
    - An art lease with a rental period and delivery address.
    - A stock image purchase and download.
