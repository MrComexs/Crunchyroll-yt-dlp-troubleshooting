# Crunchyroll not working with MPV
This is how to get Crunchyroll to work with MPV after installing the basic MPV, yt-dlp, and anime4k setup. For this install I used '--cookies-from-broswer' instead since '--cookies' might not work. I would recommend switch over to it. look here for a example its on like 5, be sure to replace firefox with your browser [link](#updating-yt-dlp-conf-file) 
[This is for chrome](#getting-user-agent-from-chrome)
[This is for firefox](#getting-user-agent-from-firefox)

## Getting user agent from Chrome
!!! Chrome forks
	This might also work with some Chrome forks like
	brave, chromium, edge, opera, safari, vivaldi
1. Open Chrome  and in the address bar type `chrome://version/`
2. look for the table and in column 5 on the left hand side you should see `user agent`
3. copy the value that is to the left of that column should start with `Mozilla/#.0`

the value does take two lines so don't forget the second line. Don't copy the 'User Agent:' since that is just what the value is named on the table.
here is a example
```
Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/120.0.0.0 Safari/537.36
```
now that you have done this three step head over to [Update yt-dlp.conf](#updating-yt-dlp-conf-file) 

## Getting user agent from Firefox
1. Open Firefox  and in the address bar type `about:support`
2. look for the table and in column 5 on the left hand side you should see `user agent`
3. copy the value that is to the left of that column should start with `Mozilla/#.0`

here is a example
```
Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:121.0) Gecko/20100101 Firefox/121.0
```
now that you have done this three step head over to [Update yt-dlp.conf](#updating-yt-dlp-conf-file) 

##  Updating yt-dlp conf file
4. go into you yt-dlp.conf file that is the the main MPV folder in your program files if that is were you installed it.
5. replace the existing line that starts with `--user-agent` make sure to keep the `--user-agent` and add `"` around the user agent like how it was before
the file should look something like this.
!!! note I used firefox for this example but switch it for the browser you got your user agent from.
```
--all-sub
--no-check-certificate
--extractor-args crunchyrollbeta:hardsub=none 
-f b
--cookies-from-browser firefox
--user-agent "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:121.0) Gecko/20100101 Firefox/121.0"
```

## afterwards
If the previous steps didn't work then you might have to sign into Crunchyroll on your browser where ever you pulled you user agent as well as your cookies from. If that doesn't help either then try watching a few minutes or eps in web browser then try again with mpv.

## Contact me 
If none of the steps work then try again you might have missed typed something. If that doesn't work then send me a dm. or comment on the youtube channel if that is where you can from.
