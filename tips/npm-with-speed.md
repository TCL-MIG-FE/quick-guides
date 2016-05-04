# 如何提升npm下载速度

默认情况下，利用`npm install`下载资源时，默认会从[npm官方][1]进行下载。由于服务器在国外，所以速度会慢很多。我们可以将`npm`的下资源指向[淘宝npm源][2]来提高下载速度。

```bash
C:\Users\lzhao>npm config get registry
https://registry.npmjs.org/

C:\Users\lzhao>npm config set registry http://registry.npm.taobao.org/

C:\Users\lzhao>npm config get registry
http://registry.npm.taobao.org/

C:\Users\lzhao>
```

当然，我们也可以下载[nrm][3]这个工具更快速地切换下载源。

```bash
C:\Users\lzhao>npm install -g nrm
```

```
C:\Users\lzhao>nrm ls

* npm ---- https://registry.npmjs.org/
  cnpm --- http://r.cnpmjs.org/
  taobao - http://registry.npm.taobao.org/
  edunpm - http://registry.enpmjs.org/
  eu ----- http://registry.npmjs.eu/
  au ----- http://registry.npmjs.org.au/
  sl ----- http://npm.strongloop.com/
  nj ----- https://registry.nodejitsu.com/
  pt ----- http://registry.npmjs.pt/
  tcl ---- http://npm.tcl.com:8000/


C:\Users\lzhao>nrm use taobao

   Registry has been set to: http://registry.npm.taobao.org/

C:\Users\lzhao>nrm ls

  npm ---- https://registry.npmjs.org/
  cnpm --- http://r.cnpmjs.org/
* taobao - http://registry.npm.taobao.org/
  edunpm - http://registry.enpmjs.org/
  eu ----- http://registry.npmjs.eu/
  au ----- http://registry.npmjs.org.au/
  sl ----- http://npm.strongloop.com/
  nj ----- https://registry.nodejitsu.com/
  pt ----- http://registry.npmjs.pt/
  tcl ---- http://npm.tcl.com:8000/

C:\Users\lzhao>

```




[1]: https://www.npmjs.com/
[2]: http://registry.npm.taobao.org/
[3]: https://www.npmjs.com/package/nrm
