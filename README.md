# Yasmine

Yasmine (Yet Another Station Metadata INformation Editor), is a Python web application to create and edit geophysical station metadata information in FDSN stationXML format.
This is a joint development of IRIS and Résif.
Development and addition of new features is shared and agreed upon between IRIS and Résif.


## Known issues
Even if we have performed a lot of tests, Yasmine is currently released in beta version and some bugs and limitations might still be found.

Installation setup currently fails with `numpy-1.22.2`. It is recommended to use `numpy-1.21.5` instead.

The new **AROL** (Atomic Response Objects Library) instrument response library, from Résif, is still in depoyment stage and only includes a limited set of instruments.
Users are encouraged to use the **NRL** library, also available.

## Instructions for users

### User Manual
Please read the included .docx manual for instructions on how to get started using Yasmine.

If there is no internet connection, unzip the bundled NRL (IRIS.zip) in the `data` folder at the root of this repository.

### Installation using Python
1. Install Python 3.6.5 or greater
2. Run `python -m venv env`
3. Run `source env/bin/activate`
4. Run `pip install --upgrade pip setuptools`
5. Run `pip install YASMINE-x.x.tar.gz`
6. Run `sudo yasmineapp.py syncdb upgrade heads`
7. Run `sudo yasmineapp.py runserver`
8. Visit <http://localhost:1841>

### Installation using Docker
1. Install [Docker Compose](https://docs.docker.com/compose/install/) or [Docker Desktop](https://www.docker.com/products/docker-desktop)
2. go in yasmine-stationxml-editor folder
3. Run start.sh
4. Visit <http://localhost:1841>
5. Run stop.sh to stop 

If you are running on an Apple M1 machine, uncomment the lines indicating the target platform in the `docker-compose.yml` file.

## Instructions for developers
1. To develop frontend, please go to `frontend` folder and see `README.md` file
2. To develop backend, please go to `backend` folder and see `README.md` file


## More information
* [Incorporated Research Institutions for Seismology (IRIS) Data Services](https://ds.iris.edu)
* [réseau sismologique et géodésique français (Résif)](https://www.resif.fr/)
* [FDSN StationXML Manual](https://stationxml-doc.readthedocs.io/en/release-1.1.0/)
* [Nominal Response Library (NRL)](https://ds.iris.edu/ds/nrl/)
