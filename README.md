SQLiv
===

### Massive SQL injection scanner
**Features**
1. multiple domain scanning with SQL injection dork
2. targetted scanning by providing specific domain (with crawling)
4. reverse domain scanning

---

**1. Multiple domain scanning with SQLi dork**  
- it simply search multiple websites from given dork and scan the results one by one
```python
python sqliv.py -d <SQLI DORK> -e <SEARCH ENGINE>  
python sqliv.py -d "inurl:index.php?id=" -e google  
```

**2. Targetted scanning**  
- can provide only domain name or specifc url with query params
- if only domain name is provided, it will crawl and get urls with query
- then scan the urls one by one
```python
python sqliv.py -t <URL>  
python sqliv.py -t www.example.com  
python sqliv.py -t www.example.com/index.php?id=1  
```

**3. Reverse domain and scanning**
- do reverse domain and look for websites that hosted on same server as target url
```python
python sqliv.py -t <URL> -r
```

**python sqliv.py --help**
```python
usage: sqliv.py [-h] [-d D] [-e E] [-p P] [-t T] [-r]

optional arguments:
  -h, --help \ show this help message and exit
  -d D\ \ \ \ \ \ \ \ SQL injection dork
  -e E\ \ \ \ \ \ \ \ search engine [Google only for now]
  -p P\ \ \ \ \ \ \ \ number of websites to look for in search engine
  -t T\ \ \ \ \ \ \ \ scan target website
  -r\ \ \ \ \ \ \ \ \ reverse domain
```
