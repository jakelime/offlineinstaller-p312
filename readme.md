# offlineinstaller-p312

offline installer for python3.12

Built for `win10`

## Sytstem information

```python
platform.platform()='Windows-10-10.0.22621-SP0'
platform.system()='Windows'
platform.machine()='AMD64'
platform.uname()=uname_result(system='Windows', node='HLZBP02', release='10', version='10.0.22621', machine='AMD64')
```

## Instructions

1. Create requirements using `venv`

   ```powershell
   python -m venv venv
   .\venv\Scripts\activate
   pip install .. .. ..
   pip freeze > requirements.txt
   ```

1. Download as offline packages

   ```powershell
   pip download --dest .\downloaded_wheels\ -r .\requirements.txt
   ```

1. On the offline system, use `pip install --no-index --find-links /path/to/download/dir/ -r requirements.txt`

   ```powershell
   git clone https://github.com/jakelime/offlineinstaller-p312.git
   cd .\offlineinstaller-p312
   pip install --no-index --find-links .\downloaded_wheels\ -r requirements.txt
   ```
