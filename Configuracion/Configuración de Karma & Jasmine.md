## Launchers:

Los **launchers** son componentes que permiten ejecutar las pruebas unitarias y de integración escritas en Jasmine (u otros frameworks de pruebas) en diferentes navegadores o entornos de ejecución.

La configuración estándar ejecuta las pruebas en el navegador Chrome. Para ejecutar las pruebas en otros navegadores, necesitamos instalar diferentes **Launchers** .

Para instalar otros lanzadores, primero debemos instalar el paquete npm respectivo.

Firefox:
```shell
$ npm install karma-firefox-launcher --save-dev
```

- Documentación: https://www.npmjs.com/package/karma-firefox-launcher

Safari:
```shell
$ npm install karma-safari-launcher --save-dev
```

- Documentación: https://www.npmjs.com/package/karma-safari-launcher

Internet Explorer:
```shell
$ npm install karma-ie-launcher --save-dev
```

- Documentación: https://www.npmjs.com/package/karma-ie-launcher 

Opera:
```shell
$ npm install karma-opera-launcher --save-dev
```

- Documentación: https://www.npmjs.com/package/karma-opera-launcher

Cada **launcher** debe configurarse en el archivo de configuración de karma karma.conf.js :

```shell
plugins: [
  require('karma-jasmine'),
  require('karma-chrome-launcher'),
  require('karma-firefox-launcher'),
  require('karma-safari-launcher'),
  require('karma-jasmine-html-reporter'),
  require('karma-coverage'),
  require('@angular-devkit/build-angular/plugins/karma')
  ]
```

Para poder ejecutar las pruebas en diferentes **Browsers** también debemos agregarlos a la configuración en el listado de **Browsers**
```shell
browsers: ['Chrome', 'Firefox', 'Safari']
```


## Reporters:


