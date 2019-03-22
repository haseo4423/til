### マージメッセージからリリースノートを作成する

##### .git/configファイル

```
[alias]
  releasenote = "!f () {\
    git log --date=short --merges --pretty=format:\"[%cd] %b%+\" origin/master 3.1.2.. > releasenote.txt;\
  };f"
```

##### homeディレクトリ/XXXX_release_note.sh

```
#!/bin/sh

cd git/XXXX
git releasenote today
cp releasenote.txt ~
```
