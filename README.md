# DataVission
להתחלה- עשינו קובץ py
```python
import psutil
from flask import Flask, render_template

app = Flask(_name_)

@app.route("/")
def index():
    cpu_metric = psutil.cpu_percent()
    mem_metric = psutil.virtual_memory().percent
    Message = None
    if cpu_metric > 80 or mem_metric > 80:
        Message = "High CPU or Memory Detected, scale up!!!"
    return render_template("index.html", cpu_metric=cpu_metric, mem_metric=mem_metric, message=Message)

if _name=='__main_':
    app.run(debug=True, host = '0.0.0.0')
```
