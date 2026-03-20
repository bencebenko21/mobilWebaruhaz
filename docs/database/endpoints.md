### Homepage

#### GET /api/products/new/
- **Description**: returns products that are new
- **Access**: public

#### GET /api/products/sale/
- **Description**: returns products that are on sale
- **Access**: public

#### GET /api/products/outgoing/
- **Description**: returns products that are outgoing
- **Access**: public

### Products page

#### GET /api/products/
- **Description**:  in products page returns all products unfiltered
- **Access**: public 

#### GET /api/products/?brand=1&color=1&size=1&storage=1
- **Description**:  returns filtered products the user selected
- **Access**: public

#### GET /api/makes/
- **Description**: returns make, populates the filter lists
- **Access**: public

#### GET /api/colors/
- **Description**: returns colors, populates the filter lists
- **Access**: public

#### GET /api/sizes/
- **Description**: returns sizes, populates the filter lists
- **Access**: public

#### GET /api/storage/
- **Description**: returns storage options, populates the filter lists
- **Access**: public

### Product detail
#### GET /api/products/{id}/
- **Description**: returns all the details needed for a specific product (size, storage, name, line, description)
- **Access**: public

#### GET /api/products/{id}/variants/
- **Description**: returns the variant the user selected from the filters
- **Access**: public

#### GET /api/variants/{id}/
- **Description**: populate the filters with the variants in storage and color
- **Access**: public

#### POST /api/cart/items/
- **Description**: Adds the item to the cart
- **Access**: registered user

### Cart

#### GET /api/cart/
- **Description**: returns elements in the cart when loaded cart page
- **Access**: registered user

#### PATCH /api/cart/items/{id}/
- **Description**: adding items (or decreasing items) using + and - buttons in cart
- **Access**: registered user

#### DELETE /api/cart/items/{id}/
- **Description**: removing an item from cart
- **Access**: registered user

#### POST /api/orders/
- **Description**: when pushing order item create an order
- **Access**: registered user


### Auth
#### POST /api/auth/login/
- **Description**: after entering credentials (email and password) login (change auth of user to logged in)
- **Access**: public

#### POST /api/auth/register/
- **Description**: register using entered credentials
- **Access**: public

#### POST /api/auth/logout/
- **Description**: logout of session
- **Access**: registered user

### Admin

#### POST /api/products/
- **Description**: creates new product 
- **Access**: admin

#### PUT /api/products/{id}/
- **Description**: updates a product page
- **Access**: admin

#### DELETE /api/products/{id}/
- **Description**: deletes a product from page
- **Access**: admin
#### PATCH /api/inventory/{id}/
- **Description**: updates inventory when shipment comes
- **Access**: admin
