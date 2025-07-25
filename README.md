# Express Product API

## Setup
1. Clone the repo
2. Run `npm install`
3. Create a `.env` file from `.env.example` and set your `API_KEY`
4. Start server: `node server.js`

## API Endpoints

### `GET /api/products`
- List all products
- Supports: `?category=electronics`, `?search=phone`, `?page=1&limit=2`

### `GET /api/products/:id`
- Get product by ID

### `POST /api/products`
- Create product
- Requires: `name`, `description`, `price`, `category`, `inStock`
- Header: `x-api-key: YOUR_API_KEY`

### `PUT /api/products/:id`
- Update existing product

### `DELETE /api/products/:id`
- Delete product

### `GET /api/products/stats`
- Get product count by category

## Example
```bash
curl -X GET http://localhost:3000/api/products -H "x-api-key: your_api_key_here"
