[![DOI](https://img.shields.io/badge/DOI-doi.org%2F10.1063%2F5.0008368-blue)](https://aip.scitation.org/doi/10.1063/5.0008368)

# pychemcurv-app

This repository contains a web application using the [pychemcurv module](https://github.com/gVallverdu/pychemcurv)
for local curvature analyzes of molecules. It aims to use the pychemcurv 
package and visualize the geometrical or chemical atomic quantities mapped on 
the chemical structure of your system.

The application is available at this address: https://pychemcurv.herokuapp.com/

Demo video:

[![youtube demo video](https://img.youtube.com/vi/q7UO5Gou-lw/0.jpg)](https://www.youtube.com/watch?v=q7UO5Gou-lw)

## Citing pychemcurv

Please consider to cite the following paper when using the application or the
[pychemcurv module](https://github.com/gVallverdu/pychemcurv).

* Julia Sabalot-Cuzzubbo, Germain Salvato Vallverdu, Didier Bégué and Jacky Cresson
*Relating the molecular topology and local geometry: Haddon’s pyramidalization angle and the Gaussian curvature*, 
J. Chem. Phys. **152**, 244310 (2020).

[![DOI](https://img.shields.io/badge/DOI-doi.org%2F10.1063%2F5.0008368-blue)](https://aip.scitation.org/doi/10.1063/5.0008368)

## Run the application locally

You can run the application locally once you have installed pychemcurv and
the dash dependencies of the application. The easiest way to this is to use
the `requirements.txt` or the `environment.yml` files to set up a python 
environment.

Using pip

    pip install -r requirements.txt

Using conda

    conda env create -f environment.yml

This will create an environment named `curv` and install all dependecies. 
Then, to run the application, change to `pychemcurv/app` folder and run the
`app.py` file.

    conda activate curv
    python app.py

This will output something like this. Open the url to use the application.

    [user@computer] (curv) > $ python app.py
    Running on http://127.0.0.1:8050/
    Debugger PIN: 065-022-191
    * Serving Flask app "app" (lazy loading)
    * Environment: production
    WARNING: This is a development server. Do not use it in a production deployment.
    Use a production WSGI server instead.
    * Debug mode: on

You can switch off the debug mode by setting `debug=False` on the last line of 
the `app.py` file.

### Common error if running application locally

If the application does not start with an error such as:

```sh
socket.gaierror: [Errno 8] nodename nor servname provided, or not known
```

Go to the last lines of the file app.py and comment/uncomment the last
lines to get something that reads

```py
if __name__ == '__main__':
    app.run_server(debug=True, host='127.0.0.1')
    # app.run_server(debug=False)
```

## TODO

* Manage file format
* Manage periodic structure
* Show/Hide atom names = species + index
* Ball and stick representation
* Zoom fit the box at the beginning

## Licence and contact

This software was developped at the [Université de Pau et des Pays de l'Adour (UPPA)](http://www.univ-pau.fr)
in the [Institut des Sciences Analytiques et de Physico-Chimie pour l'Environement et les Matériaux (IPREM)](http://iprem.univ-pau.fr)
and the [Institut Pluridisciplinaire de Recherches Appliquées (IPRA)](http://ipra.univ-pau.fr/) and is distributed under the 
[MIT licence](https://opensource.org/licenses/MIT).

## Authors

* Germain Salvato Vallverdu: `germain.vallverdu@univ-pau.fr <germain.vallverdu@univ-pau.fr>`_
* Julia Sabalot-cuzzubbo `julia.sabalot@univ-pau.fr  <sabalot.julia@univ-pau.fr>`_
* Didier Bégué: `didier.begue@univ-pau.fr <didier.begue@univ-pau.fr>`_
* Jacky Cresson: `jacky.cresson@univ-pau.fr <jacky.cresson@univ-pau.fr>`_

