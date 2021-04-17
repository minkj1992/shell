# 유용한 스크립트

## github wget

- $ wget -O <폴더>/<파일이름> <github raw url>

```bash
$ wget -O ./kocoon-hermes/values.yaml https://github.daumkakao.com/raw/~~~
```

## grep && replace

```bash
$ BASEDIR='./dkosv3/sandbox'
$ CLUSTER_NAME=$(kubectl config current-context | sed -e 's/-context$//')
$ wget -O $BASEDIR/kocoon-hermes/values.yaml https://github.daumkakao.com/raw/~~~
$ grep -rl "changeme" $BASEDIR/kocoon-hermes | xargs sed -i '' 's/changeme/'"$CLUSTER_NAME"'/g'
```

## find by file name (recursive)

```bash
$ find . -name '*.java'
```
