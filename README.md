# Locale en_NL

I wanted a custom locale for my desktop. Most stuff is straight from en_US, but I've made some modifications.

Most relevantly, the decimal separator is a period and thosuand separator a comma.

## Installing
On Fedora 39, copy the file `en_NL` to `/usr/share/i18n/locales`

Then, compile and select it:

```sh
sudo localedef --no-archive -i en_NL -f UTF-8 en_NL.UTF-8
sudo localectl set-locale en_NL.UTF-8
gsettings set org.gnome.system.locale region "en_NL.utf8"
```

Then logout and log back in and everything should be changed.

## Thanks

Many thanks to [this answer on Unix Stack Exchange](https://unix.stackexchange.com/a/197693/38945)
