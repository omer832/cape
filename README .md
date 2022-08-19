# CAPEv2-API

This API will an analyze uploaded file with CAPEv2 and return analysis result as JSON files

## Setup CAPEv2
You can start by downloading this repo with git command below
```
  git clone https://github.com/omer832/cape.git
```


[CAPEv2 ](https://github.com/kevoreilly/CAPEv2)



## Run cape



```bash
sudo python3 utils/rooter.py -g cape
```



```bash
sudo -u cape python3 cuckoo.py 
```



```bash
sudo -u cape  python3 utils/process.py -p7 auto
```
## Run API

```bash
python3 main.py
```
### You can send your file request using command below
- This request gives you a task id

```bash
curl -F file=@/path/to/file http://127.0.0.1:5000/file-upload
```
### You can get your analysis report with your task id using command below

```bash
curl -L "http://0.0.0.0:8000/apiv2/tasks/get/report/<your_task_id>/json"
```

  