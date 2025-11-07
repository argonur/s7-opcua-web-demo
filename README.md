# s7-opcua-web-demo
Example project showing how to connect a Siemens S7 PLC (via PLCSIM Advanced and OPC UA) to a simple web-based HMI using Python. Includes OPC UA client, web server, and browser interface.

---

# Backend
To start the backend service, the following steps are required:
* Access the backend/ directory
* Load the backend virtual environment:
```bash
source *nombre-del-entorno*/bin/activate
```

* Start the service:
```bash
uvicorn main:app --reload
```

- A screen similar to this one is expected on the terminal:
```bash
❯ uvicorn main:app --reload
INFO:     Will watch for changes in these directories: ['/home/user-pc/github/plc-remote/backend']
INFO:     Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)
INFO:     Started reloader process [63260] using StatReload
INFO:     Started server process [63262]
INFO:     Waiting for application startup.
```

---

# Frontend
To start the frontend service, the following steps are required:
* Access the frontend/ directory
* Start the service:
```bash
npm run dev
```

* You should see a screen similar to this one on the terminal:
```bash
  VITE v7.1.12  ready in 346 ms

  ➜  Local:   http://localhost:5173/
  ➜  Network: use --host to expose
  ➜  press h + enter to show help
```
---

To configure the project settings with respect to the elements that make up the PLC, see `docs/customization`