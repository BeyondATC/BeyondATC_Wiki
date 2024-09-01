# Known issues

???+ bug "Readback issues on frequencies"
    Frequencies readbacks can be misunderstood by BeyondATC. This is mostly due to the *decimal* word

    **WORKAROUND**: You can readback frequencies without saying decimal. 121.95 would be said as *12195*. Or you can use *point* instead of decimal.

??? bug "Auto respond/click response is not understood by the controller"
    Auto respond or the click response when tuning tower might not be understood by the tower controller, mostly because the request triggered is *holding short runway XX* and it is expecting to receive *ready for departure*.

    **WORKAROUND**: You need to trigger multiple times the response, it will change it after a few attempts. Or you can request departure with your voice.

??? bug "Can't change the runway on arrival, it says that I wasn't assigned a runway yet"
    You can request a runway change **when the controller tells you the first time which runway to expect**. The subsequent messages from the controller is wrong, and should just tell you that you can't change anymore.