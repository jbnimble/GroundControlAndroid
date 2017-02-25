# GroundControlAndroid
The APK built for Android from https://github.com/MaslowCNC/GroundControl using Kivy Buildozer

Created using version with latest pull request: https://github.com/MaslowCNC/GroundControl/pull/83

Instructions to create APK (effectively these instructions https://buildozer.readthedocs.io/en/latest/quickstart.html):
 * Download Buildozer VM, run in VirtualBox
 * Upgrade Buildozer: $ sudo pip install --upgrade buildozer
 * Download, extract, and change directory to Ground Control ZIP: https://github.com/MaslowCNC/GroundControl
 * Add version to main.py (right above if __name__=='__main__'): __version__ = "0.83"
 * Initialize Buildozer: buildozer init
 * Modify buildozer.spec:
    title = Ground Control
    package.name = groundcontrol
    package.domain = com.github.maslowcnc
    requirements = pyserial,kivy
    android.p4a_whitelist = lib-dynload/termios.so
 * Build APK: $ buildozer -v android debug
 * APK will be in 'bin' directory, load onto Android device
