```
ssh -i "~/.ssh/キー" centos@パブリックドメイン
cd exist-master/
python3 manage.py runserver パブリックドメイン:8000
python3 scripts/insert2db/reputation/insert2db.py
```
