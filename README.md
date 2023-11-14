[![DOI](https://img.shields.io/badge/DOI-doi.org%2F10.1063%2F5.0008368-blue)](https://aip.scitation.org/doi/10.1063/5.0008368)

# pychemcurv-app

This repository contains a web application using the [pychemcurv module](https://github.com/gVallverdu/pychemcurv)
for local curvature analyzes of molecules. It aims to use the pychemcurv 
package and visualize the geometrical or chemical atomic quantities mapped on 
the chemical structure of your system.

The live demo of the application is available here: https://pychemcurv.onrender.com

Demo video:

[![youtube demo video](https://img.youtube.com/vi/q7UO5Gou-lw/0.jpg)](https://www.youtube.com/watch?v=q7UO5Gou-lw)

## Run the application locally

You can run the application locally once you have installed pychemcurv and
the dash dependencies of the application. The easiest way to this is to use
the `requirements.txt` or the `environment.yml` files to set up a python 
environment.

Using pip, after you create a new environment

    pip install -r requirements.txt

Using conda, the following will create a new environment named `curv` and
install all dependencies inside, including pychemcurv.

    conda env create -f environment.yml

Then, download the application and run it by executing the 
`app.py` file.

```sh
git clone https://github.com/gVallverdu/pychemcurv-app.git
cd pychemcurv-app
conda activate curv   # if you need to activate an environment
python app.py
```

This will output something like this. Open the url http://127.0.0.1:8050/ 
(or the one provided in the terminal) to use the application.

```sh
[user@computer] (curv) > $ python app.py
Running on http://127.0.0.1:8050/

Debugger PIN: 065-022-191
* Serving Flask app "app" (lazy loading)
* Environment: production
  WARNING: This is a development server. Do not use it in a production deployment.
  Use a production WSGI server instead.
* Debug mode: on
````

You can switch off the debug mode by setting `debug=False` on the last line of 
the `app.py` file.

### Common error when running the application locally

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

There you can also switch on and off the debug mode keeping the `host` url.

and run the application again.

## TODO

* Manage file format
* Manage periodic structure
* Show/Hide atom names = species + index
* Ball and stick representation
* Zoom fit the box at the beginning

## Citing pychemcurv

Please consider to cite the following paper when using the application or the
[pychemcurv module](https://github.com/gVallverdu/pychemcurv).

* Julia Sabalot-Cuzzubbo, Germain Salvato Vallverdu, Didier Bégué and Jacky Cresson
*Relating the molecular topology and local geometry: Haddon’s pyramidalization angle and the Gaussian curvature*, 
J. Chem. Phys. **152**, 244310 (2020).

[![DOI](https://img.shields.io/badge/DOI-doi.org%2F10.1063%2F5.0008368-blue)](https://aip.scitation.org/doi/10.1063/5.0008368)

* Julia Sabalot-Cuzzubbo, N. Cresson, Germain Salvato Vallverdu, Didier Bégué and Jacky Cresson
*Haddon’s POAV2 vs POAV theory for non-planar molecules*, 
J. Chem. Phys. **159**, 174109 (2023).

[![DOI](https://img.shields.io/badge/DOI-doi.org%2F10.1063%2F5.0008368-blue)](https://aip.scitation.org/doi/10.1063/5.0170800)


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

