# Example

* Build the webapp package using the following command:
```bash
cd ./webapp
python3 -m pip install --upgrade setuptools wheel build
python3 -m build
```
* This generates a wheel file (.whl) in dist/ folder:
```bash
ls -l dist/
```
![img.png](./img/dist-folder.png)
* Build the docker image
```bash
docker build -t ghcr.io/YOUR_USER/simple-webapp:latest .
```
* Run the docker image and open the webapp in your browser [http://localhost:8000](http://localhost:8000):
```bash
docker run -it -p 8000:8000 ghcr.io/YOUR_USER/simple-webapp:latest
```
