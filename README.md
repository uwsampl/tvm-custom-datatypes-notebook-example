This Docker container runs a Jupyter notebook containing an example of the TVM custom datatypes work (also known as Bring Your Own Datatypes).

# Running

```bash
git clone <this repo>
cd <this repo>
# Build Docker image from Dockerfile
docker build  -t tvm-custom-datatypes-notebook-example  -f Dockerfile .
# Run Docker image (which starts a Jupyter Notebook server)
# Note that the -p option is important for connecting host port 8888 to your
# Docker container's port 8888.
docker container run -i -p 8888:8888 --rm -t \
  tvm-custom-datatypes-notebook-example:latest
```

In the output, you should see something like:
```
[C 21:21:25.581 NotebookApp] 
    
    To access the notebook, open this file in a browser:
        file:///root/.local/share/jupyter/runtime/nbserver-1-open.html
    Or copy and paste one of these URLs:
        http://b1fba94d05a3:8888/?token=bb495da54309d23324677dcaeed78e5ded9e8e34ccbbf9d3
     or http://127.0.0.1:8888/?token=bb495da54309d23324677dcaeed78e5ded9e8e34ccbbf9d3
```

Navigate to the last address (the one using `127.0.0.1`) in your browser, and the notebook should open!
