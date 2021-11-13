
## Installation
### 1. Requirements
- Python 3.7+
- python cryptography module
- ffmpeg

### 2. Installation
- Download source
- Unzip source in the installation folder
- Create a data folder inside the installation folder and create a config.ini file inside the data folder
- Edit the config.ini and add the following lines
<pre>
[plutotv_default]
label = PlutoTV Instance
</pre>
- OS specific installation help can be found in lib/tvheadend/service (eg CoreELEC, Windows, etc)
- Launch the app by running the command "python3 tvh_main.py"
- Bring up browser and go to http://ipaddress:6077/
- Go to settings and make changes you want.
    - Logging: Change log level from warning to info if needed
    - Under Providers > PlutoTV enable
        - URL Filtering
        - PTS/DTS Resync
- From XML/JSON Links try some of the links

### 3. Notes
- URL used can include plugin and instance levels to filter down to a specific set of data
    - http://ipaddress:6077/channels.m3u
    - http://ipaddress:6077/pLuToTv/channels.m3u
    - http://ipaddress:6077/PlutoTV/Default/channels.m3u
- config.ini group tag requirements
    - All lower case
    - Underscore separates the plugin name from the instance name
    - Use a single word if possible for the instance name or use underlines between words
    - Do not change the instance name.  It is used throughout the system and is difficult to change.
    - [plutotv_mychannels]

Enjoy
