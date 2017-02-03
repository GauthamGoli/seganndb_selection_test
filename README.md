

### Installing SegannDB

 * Installing SegannDB is straightforward. I just followed the instructions specified in [INSTALL.sh](https://github.com/tdhock/SegAnnDB/blob/master/INSTALL.sh) and was able to get it installed.

### Uploading datasets into SegannDB Server instance

 * I downloaded this dataset [http://members.cbio.mines-paristech.fr/~thocking/data/aichi-backup.tgz](http://members.cbio.mines-paristech.fr/~thocking/data/aichi-backup.tgz)
 * Uploaded it using [upload_profiles.py](https://github.com/tdhock/SegAnnDB/blob/master/plotter/static/upload_profiles.py) by executing the below command
 * ```$ find /home/xz0r/Downloads/aichi-backup/ -name "*.gz" -exec python ./plotter/static/upload_profiles.py http://localhost:8080 seganntest@gmail.com {} + ```
 * The above command passes the files with ```.gz``` extension in the provided directory as arguments to ```upload_profiles.py``` script
 * Screen cast demonstrating annotation: [https://youtu.be/UJgk-R96aQo](https://youtu.be/UJgk-R96aQo)

### Setting up headless brower testing framework

 * ``` $ pip install selenium```
 *  Download latest version of geckodriver and add it to PATH
 *  ```$ python tests.py```
 *  Screen cast of the tests: [https://www.youtube.com/watch?v=ydeLQ772sS4](https://www.youtube.com/watch?v=ydeLQ772sS4)

### Codecoverage

 * Not yet implemented.
 * I intend to implement it by initially setting up a build environment in [Travis-CI](http://travis-ci.org/) and [codecov.io](https://codecov.io/) 
 * Since we have selenium based unit tests or Functional tests to be precise, Travis-CI has [GUI and Headless Browser Testing](https://docs.travis-ci.com/user/gui-and-headless-browsers/) and selenium can be easily integrated using [Sauce labs](https://saucelabs.com/) add on in Travis-CI.
