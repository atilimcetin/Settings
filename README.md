Settings
========

The Settings class provides persistent platform-independent application settings.


`Settings.new()` Creates a new Settings object. 

`Settings:set(key, value)` Sets the value of setting key to value. If the key already exists, the previous value is overwritten.

`Settings:get(key, defaultValue)` Returns the value for setting key. If the setting doesn't exist, returns defaultValue. If no default value is specified, nil is returned.

`Settings:contains(key)` Returns true if there exists a setting called key; returns false otherwis

`Settings:remove(key)` Removes the setting key.

`Settings:sync()` Writes any unsaved changes to permanent storage. This function is called automatically when the application suspends or exits, so you normally don't need to call it yourself.


Here is a sample usage:

	local settings = Settings.new()
	settings:get("current_level", 1)
	settings:set("current_level", 2)
