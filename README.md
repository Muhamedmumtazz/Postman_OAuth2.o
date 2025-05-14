# OAuth Project - Postman API Test Suite

This project demonstrates how to test an OAuth 2.0-secured API using Postman. It includes the flow of obtaining an authorization code, exchanging it for an access token, and using that token to make authenticated API requests.

---

## 📁 Project Structure

This Postman collection includes:

1. **getCode**  
   A `GET` request simulating the OAuth redirect to retrieve the authorization code.

2. **ExchangeCode**  
   A `POST` request to exchange the authorization code for an access token.

3. **ActualRequest**  
   A `GET` request that uses the access token to call a protected endpoint and validates the response using Postman test scripts.

4. **random**  
   An extra sample request hitting the same endpoint with hardcoded code parameters.

---

## 🔐 OAuth 2.0 Authentication Flow

This project uses the **Authorization Code Grant Flow**:

1. **Authorization Request**: You retrieve a `code` by simulating a login (already hardcoded in `getCode`).
2. **Token Exchange**: The code is exchanged for an `access_token` via the `ExchangeCode` request.
3. **API Call**: The token is used to authenticate requests in `ActualRequest`.

---

## 🧪 Test Validations

The `ActualRequest` includes Postman tests to:

- ✅ Verify if the course "Cypress" exists.
- ✅ Ensure the Cypress course object contains `courseTitle` and `price`.
- ✅ Validate that the sum of all API course prices equals `90`.
- ✅ Match the actual Web Automation course titles with expected titles:  
  `["Selenium Webdriver Java", "Cypress", "Protractor"]`

---

## 🚀 How to Use

### 1. Clone this Repository
```bash
git clone https://github.com/your-username/oauth-postman-project.git
cd oauth-postman-project
