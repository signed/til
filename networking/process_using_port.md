# How to find the process using a given port
Given the port we are interested is 2202
## MacOs

```bash
ps -ax | grep `lsof -t -i :2202`
```
