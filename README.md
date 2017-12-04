# Yii2 Pretty URL

## First Step
Enable the **'urlManager'** in **../config/web.php**

## Second Step
Add configurations inside **'urlManager'**

```
'urlManager' => [
            'enablePrettyUrl' => true,
            'showScriptName' => false,
            'rules' => array(
                'index' => 'site/index',
                '<controller:\w+>/<id:\d+>' => '<controller>/view',
                '<controller:\w+>/<action:\w+>/<id:\d+>' => '<controller>/<action>',
                '<controller:\w+>/<action:\w+>' => '<controller>/<action>',
            ),
        ],
```

## Last Step
Add file [*.htaccess*](https://github.com/kevingatp/Yii2-Pretty-URL/blob/master/basic/web/.htaccess) into dir **web**, you can copy the file from this repo

###### note:
* Default URL for login
```
http://localhost/basic/web/index.php?r=site%2Flogin
```
* After enable Pretty URL you can access login through
```
http://localhost/basic/web/site/login
```
