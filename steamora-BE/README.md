## Steamora Back-End

Back end for Steamora.


### Build and Run

#### Using CMake

##### Pre Requirements

- `oatpp` 
- `oatpp-swagger`
- `oatpp-sqlite`

If required oatpp modules aren't installed, run:

```bash
chmod +x script/install-oatpp.sh
sudo ./script/install-oatpp.sh
```

##### Build Project

To build the project, run:

```bash
mkdir build && cd build
cmake .. && cmake --build .
```

Then run the server:
```bash
./steamora-BE-exe
```

---

### Endpoints 

#### HTML

|HTTP Method|URL|Description|
|---|---|---|
|`GET`|http://localhost:8000/ | Root page |
|`GET`|http://localhost:8000/swagger/ui | Swagger UI page |

#### User Service

|HTTP Method|URL|Description|
|---|---|---|
|`POST`|http://localhost:8000/users | Create new User |
|`PUT`|http://localhost:8000/users/{userId} | Update User by ID |
|`GET`|http://localhost:8000/users/{userId} | Get User by ID |
|`DELETE`|http://localhost:8000/users/{userId} | Delete User by ID |
|`GET`|http://localhost:8000/users/offset/{offset}/limit/{limit} | Get All Users with Paging |
