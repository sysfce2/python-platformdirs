# appdirs Changelog

## appdirs 1.1.0 (not yet released)

- Add `appdirs.AppDirs` convenience class. Usage:

        >>> dirs = AppDirs("SuperApp", "Acme", version="1.0")
        >>> dirs.user_data_dir
        '/Users/trentm/Library/Application Support/SuperApp/1.0'

- [Windows] Cherry-pick Komodo's change to downgrade paths to the Windows short
  paths if there are high bit chars.
- Change default `user_cache_dir()` on Linux to be singular, e.g. "~/.superapp/cache".
- Add `roaming` option to `user_data_dir()` (for use on Windows only) and change
  the default `user_data_dir` behaviour to use a *non*-roaming profile dir
  (`CSIDL_LOCAL_APPDATA` instead of `CSIDL_APPDATA`). Why? Because a large
  roaming profile can cause login speed issues. The "only syncs on logout"
  behaviour can cause surprises in appdata info.


## appdirs 1.0.1 (never released)

Started this changelog 27 July 2010. Before that this module originated in the
[Komodo](http://www.activestate.com/komodo) product as `applib.py` and then as
[applib/location.py](http://github.com/ActiveState/applib/blob/master/applib/location.py)
(used by PyPM in [ActivePython](http://www.activestate.com/activepython)). This
is basically a fork of applib.py 1.0.1 and applib/location.py 1.0.1.
