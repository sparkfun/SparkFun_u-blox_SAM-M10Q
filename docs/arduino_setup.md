The SAM-M10Q works with the latest version of the SparkFun u-blox GNSS Arduino Library, v3. Install the library using Arduino's Library Manager Tool by searching for <b>'SparkFun u-blox GNSS v3'</b>. If you prefer to manually install the library you can download the [GitHub repository](https://github.com/sparkfun/SparkFun_u-blox_GNSS_v3) or download a ZIP of it here:

<center>
[SparkFun u-blox GNSS v3 (ZIP)](https://github.com/sparkfun/SparkFun_u-blox_GNSS_v3/archive/refs/heads/main.zip){ .md-button .md-button--primary }
</center>

The third version of this library complies with u-blox's updated UBX protocol that depreciates the UBX-CFG commands. These still work but are depreciated and u-blox now recommends using the updated VALSET, VALGET, and VALDEL commands included in v3 of the library. With the library installed, let's move on to taking a look at a couple of examples from the library.