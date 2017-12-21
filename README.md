## Building WPEWebKit

Install the dependencies by running the following command:
```
Tools/wpe/install-dependencies
```

Then run the following command to build additional dependencies:
```
Tools/Scripts/update-webkitwpe-libs
```

Run the following command to build WebKit with debugging symbols for WPE port:

```
Tools/Scripts/build-webkit --debug --wpe
```

## Running WPEWebKit
If it is not already the case, you will need to execute a **Wayland compositor**.

To do this quickly,

    $ weston --socket=wpe

Then, to run WPEWebKit:

    $ WAYLAND_DISPLAY=wpe Tools/Scripts/run-minibrowser --wpe
    $ WAYLAND_DISPLAY=wpe Tools/Scripts/run-minibrowser --wpe http://www.bouncyballs.org
