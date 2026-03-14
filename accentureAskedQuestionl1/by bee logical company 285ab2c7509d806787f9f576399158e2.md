# by bee logical company

jwt
expire time in jwt
access
refresh
axios
micro and macro task
rtk
react query
custom hook and custom component
local storage vs session cookies

## 2️⃣ Types / Differences of JWT usage

### a) **Access Token vs Refresh Token**

| Token | Purpose | Expiry | Where Used |
| --- | --- | --- | --- |
| **Access Token** | Authorize requests | Short-lived (e.g., 15 min) | Sent with API requests (in headers) |
| **Refresh Token** | Get new access tokens | Long-lived (e.g., 7 days) | Usually stored securely, used to refresh access toke |

## 2️⃣ Recommended Expiry Times

| Token Type | Typical Expiry | Reason |
| --- | --- | --- |
| **Access Token** | 10–30 minutes | Short-lived to reduce risk if stolen |
| **Refresh Token** | 1–30 days | Long-lived to allow refreshing access token |
| **Single-use JWT** | Few seconds/minutes | For sensitive operations (password reset, email verification) |

> ⚡ Shorter access token life improves security. Refresh tokens are stored securely (HTTP-only cookie or secure storage).
> 

const groupedByCity = people.reduce((acc, person) => {

const { city, name } = person;

if (!acc[city]) {

acc[city] = []; // create array if city not exists

}

acc[city].push(name); // push name to city array

return acc;

}, {});

console.log(groupedByCity);

const people = [

{ name: "Alice", city: "New York" },

{ name: "Bob", city: "Los Angeles" },

{ name: "Charlie", city: "New York" },

{ name: "David", city: "Los Angeles" },

{ name: "Eve", city: "Chicago" },

];