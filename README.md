# Roger Rafa Fans Court Booking

Easily books tennis courts. 

## Usage

```
usage: Roger Rafa [options]

optional arguments:
  -h, --help            show this help message and exit
  -c CMD, --cmd CMD     check - Check availability tomorrow or book - Book available tomorrow
  -n NO, --no NO        Number of courts to book
  -t TIME, --time TIME  Time slot to book courts
  -e EMAIL, --email EMAIL
                        Email address to get reservation confirmation
```

## Example

Check availability of courts with following command:
```
$ ./RgrRafa OR $ ./RgrRafa -c check 

      _   _   __  _  _     _        _
     |_) / \ /__ |_ |_)   |_)  /\  |_ /\
     | \ \_/ \_| |_ | \   | \ /--\ | /--\

Reservations for Monday, Nov 01 2021

[+] Available courts at 6PM: [1, 2, 3, 4, 5, 6]
[+] Available courts at 7PM: [1, 2, 3, 4, 5, 6]
[+] Available courts at 8PM: []
[+] Available courts at 9PM: []
```

Book available courts with following command:
```
$ ./RgrRafa -c book -t 13

      _   _   __  _  _     _        _
     |_) / \ /__ |_ |_)   |_)  /\  |_ /\
     | \ \_/ \_| |_ | \   | \ /--\ | /--\
    

Reservations for Monday, Nov 01 2021

[+] Available courts at 1PM: [1, 2, 3, 4, 5, 6]
[+] Booking Court 6 for tommorrow at 1PM

[+] Court 6 successfully reserved for 1PM

################################################################################
[...Redacted...]
################################################################################

[+] Available courts at 1PM: [1, 2, 3, 4, 5]
[+] Booking Court 5 for tommorrow at 1PM

[+] Court 5 successfully reserved for 1PM

################################################################################
[...Redacted...]
################################################################################

================================================================================

```

## Automatically run script as crontab

For automatically reserving 2 courts for 6PM, 7PM, 8PM following crontab file can be used. Simply run `crontab -e` and add followig lines after changing the absolute path to script on your system.

```
0 18 * * * <Absolute Path to Repo>/Roger-Rafa-Fans/RgrRafa -c book -t 18 >> <Absolute Path to Repo>/Roger-Rafa-Fans/output.log
0 19 * * * <Absolute Path to Repo>/Roger-Rafa-Fans/RgrRafa -c book -t 19 >> <Absolute Path to Repo>/Roger-Rafa-Fans/output.log
0 20 * * * <Absolute Path to Repo>/Roger-Rafa-Fans/RgrRafa -c book -t 20 >> <Absolute Path to Repo>/Roger-Rafa-Fans/output.log
```




Enjoy! 😉
