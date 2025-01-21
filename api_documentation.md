# API Documentation for Kitchen Display System (KDS)

This document provides an overview of the API endpoints used in the Kitchen Display System (KDS) application. Each endpoint includes the HTTP method, path, parameters, and expected responses.

## Endpoints

### 1. Update FCM Token
- **Method**: `PATCH`
- **Endpoint**: `/customer/update-fcm-token`
- **Request Body**:
    - `body`: A map containing the FCM token.
- **Response**:
    - `HttpResponse<FCMModel>`

### 2. Get Orders
- **Method**: `GET`
- **Endpoint**: `/backoffice/orders`
- **Query Parameters**:
    - `page`: (optional) The page number for pagination.
    - `idLT`: (optional) Filter orders with ID less than this value.
    - `orderStatusId`: (optional) Filter by order status ID.
    - `itemStatus`: (optional) Filter by item status.
    - `status`: (optional) Filter by order status.
    - `statusNot`: (optional) Exclude orders with this status.
    - `type`: (optional) Filter by order type.
    - `dateGTE`: (optional) Filter orders from this date.
    - `dateLTE`: (optional) Filter orders to this date.
    - `name`: (optional) Filter by customer name.
    - `today`: (optional) Boolean to filter today's orders.
    - `per_page`: (optional) Number of orders per page.
    - `orderProviderId`: (optional) Filter by order provider ID.
    - `search`: (optional) Search key for filtering orders.
- **Response**:
    - `HttpResponse<PaginationModel<OrderResponse>?>`

### 3. Get Order Providers
- **Method**: `GET`
- **Endpoint**: `/backoffice/order-providers`
- **Response**:
    - `HttpResponse<OrderProviders>`

### 4. Prepare Order Item
- **Method**: `PATCH`
- **Endpoint**: `/backoffice/order-items/{id}/prepare`
- **Path Parameters**:
    - `id`: The ID of the order item to prepare.
- **Response**:
    - `HttpResponse<OrderItemResponseModel>`

### 5. Mark Order Item as Ready
- **Method**: `PATCH`
- **Endpoint**: `/backoffice/order-items/{id}/ready`
- **Path Parameters**:
    - `id`: The ID of the order item to mark as ready.
- **Response**:
    - `HttpResponse<OrderItemResponseModel>`

### 6. Mark Order as Ready
- **Method**: `PATCH`
- **Endpoint**: `/backoffice/orders/{id}/ready-items`
- **Path Parameters**:
    - `id`: The ID of the order to mark as ready.
- **Response**:
    - `HttpResponse<OrderResponseModel>`

### 7. Cancel Order Item
- **Method**: `PATCH`
- **Endpoint**: `/backoffice/order-items/{id}/cancel`
- **Path Parameters**:
    - `id`: The ID of the order item to cancel.
- **Request Body**:
    - `body`: A map containing cancellation details.
- **Response**:
    - `HttpResponse<OrderItemResponseModel>`

### 8. Cancel Order
- **Method**: `PATCH`
- **Endpoint**: `/backoffice/orders/{id}/cancel-items`
- **Path Parameters**:
    - `id`: The ID of the order to cancel.
- **Request Body**:
    - `body`: A map containing cancellation details.
- **Response**:
    - `HttpResponse<OrderResponseModel>`

### 9. Prepare Order
- **Method**: `PATCH`
- **Endpoint**: `/backoffice/orders/{id}/prepare-items`
- **Path Parameters**:
    - `id`: The ID of the order to prepare.
- **Response**:
    - `HttpResponse<OrderResponseModel>`

### 10. Remake Order Item
- **Method**: `POST`
- **Endpoint**: `/backoffice/order-items/{id}/remake`
- **Path Parameters**:
    - `id`: The ID of the order item to remake.
- **Request Body**:
    - `body`: A map containing remake details.
- **Response**:
    - `HttpResponse<OrderItemResponseModel>`

### 11. Check PIN
- **Method**: `POST`
- **Endpoint**: `/backoffice/auth/check-pin`
- **Request Body**: - `body`: A map containing the PIN details.
- **Response**:
    - `HttpResponse<dynamic>`

### 12. Refresh Token
- **Method**: `POST`
- **Endpoint**: `/customer/auth/refresh-token`
- **Request Body**:
    - `data`: A map containing the refresh token data.
- **Response**:
    - `HttpResponse<dynamic>`

### 13. Get Issues
- **Method**: `GET`
- **Endpoint**: `/backoffice/configs`
- **Query Parameters**:
    - `code`: (required) The code to filter issues.
- **Response**:
    - `HttpResponse<IssuesResponse>`

### 14. Support Request
- **Method**: `POST`
- **Endpoint**: `/backoffice/support`
- **Request Body**:
    - `data`: A map containing support request details.
- **Response**:
    - `HttpResponse<dynamic>`

## Conclusion

This API documentation outlines the key endpoints for the Kitchen Display System application. Each endpoint is designed to facilitate various operations related to order management, customer interactions, and system configurations. For further details or updates, please refer to the source code or contact the development team.