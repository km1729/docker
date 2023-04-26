``` docker compose up ```
실행 시 다음과 같이 두개의 컨테이너 (postgres 와 pgadmin) 이 실행 된것을 확인할 수 있다.  

## connect to DB 
### Terminal:    
```bash
psql -U postgres
```


### pgadmin4: 
http://localhost:54331/  
1. Add server  
2. General tab
   - Name: postgres  
3. Connection tab
   - Host name: postgres  
   - Username: postgres  
   - Passwrod: 1234  








## Reference:  
https://cheesecat47.github.io/programming/2021/03/07/PostgreSQL-Docker/