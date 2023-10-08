To create simple http server with python we could use a lot, and I mean A LOT of solutions. But not to make life harder for anyone, we'll use library fast api

First of all, let's install everything
``` bash
pip install fastapi
pip install uvicorn
```

Let's create simple http server to send json object from GET /
``` python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
async def root():
	return {"hello":"world"}
```

To run it we'll use uvicorn
``` bash
uvicorn main:app --reload
```

#SyncStudy