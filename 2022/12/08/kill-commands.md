# Resolve problems while programming

# Kill ports

## In Unix (linux & mac)
### _To list any process listening to the port 8080:_
```
kill $(lsof -t -i:8080)
```

### _To list any process listening to the port 8080 **more violently**:_
```
kill -9 $(lsof -t -i:8080)
```


## In Windows

1. Find process id for port 8080
    ```
    netstat -aon | findstr 8080
    TCP 0.0.0.0:8080 0.0.0.0:0 LISTEN 74747
    # 74747 is your process id
    ```
2. Kill
    ```
    taskkill /f /pid 74747
    ```

----------------------------
---------------------------

# Kill a program

## In Windows
  1. Open task manager
  2. Select and right click on the program
  3. Click on End task

## In Unix (Linux & mac)
  ```
  killall program_name
  ```

----------------------
----------------------

# Kill Temp files

## In Windows
  1. Press `Windows+R` (or Open `Run` program manually)
  2. Enter `%TEMP%` and then press enter
  3. Select all folder and files
  4. press `Shift+Delete` then press `Enter`

## In Unix (Linux & Mac)
```
cd /var/tmp
rm -r *
```
------------------------------
------------------------------

# General commands

1. `Alt + sysrq + REISUB` or `Alt + PrtScr + REISUB` is very powerful command in linux to forcefully reboot your system even if sytem is utterly broken or freezed
**"Reboot Even If System Utterly Broken"**
