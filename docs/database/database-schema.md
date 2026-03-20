Entities:

**User**
Attributes:
- First Name
- Last Name
- E-mail
- Password
- Phone number
- ZIP code
- City
- Street name
- Floor/Flat number
- Admin flag

**Product**
- Name
- Description
- Reference Line

**ProductVariant** 
- product_id
- color_id
- size_id
- storage_id
- Price (variants might have different prices — 256GB costs more than 128GB)

**Make**
- Brands -> linked to multiple products (Samsung, Apple)

**Line**
- line_id
- Name (Galaxy S, iPhone 16 series, Redmi series)
- make_id — reference to Make

**Color** 
- just a list of colors with color_id-s. Black, White, Blue etc.

**Size** 
- just a list of sizes with size-id-s.

**Storage** 
- just a list of storage options. 128GB, 256GB etc. with storage id-s

**InventoryStock**
- Stock - No. of available stock pointing to productVariant
- shipment data (date when the shipment came)

 **Cart**
 - Belongs to a User
 - LastChange - if no change was made in 1 month delete the cart
**CartItem**
- productVariant, quantity linked to Cart

**Order**
- Order number
- Status (pending, processing, shipped, delivered, cancelled)
- Belongs to a user
- Delivery Address
- Order Date

**OrderItem**
- ProductVariant
- Quantity
- Price at the time of order -> linked to order

**Complete relationship map:**

- User → Cart — One to One
- ProductVariant → InventoryStock — One to One
- Product → ProductVariant — One to Many
- Make → Line — One to Many
- User → Order — One to Many
- Cart → CartItem — One to Many
- Order → OrderItem — One to Many
- Line → Product — One to Many
- ProductVariant → CartItem — One to Many
- ProductVariant → OrderItem — One to Many