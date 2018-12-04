# SecuritySharePreferences
使用AES加密sharePreferences 的key 和Value值
```
       SecuritySharePreferences sp = new SecuritySharePreferences(context,FILE_NAME,
                MODE);
        SecuritySharePreferences.SecurityEditor editor = sp.edit();
        editor.putString(key, (String) object);
        editor.commit();
        --------------------------
        //指定加密密钥key
       SecuritySharePreferences sp = new SecuritySharePreferences(context,FILE_NAME,
                MODE,"自定义密钥值");
        SecuritySharePreferences.SecurityEditor editor = sp.edit();
        editor.putString(key, (String) object);
        editor.commit();
        ---------------------
        //取值
       SecuritySharePreferences sp=new SecuritySharePreferences(context,FILE_NAME,MODE,"密钥key");
       sp.getString(key,defValue);
       //移除
       
       SecuritySharePreferences sp = new SecuritySharePreferences(context,FILE_NAME,
                MODE);
        SecuritySharePreferences.SecurityEditor editor = sp.edit();
        editor.remove(key);
        editor.commit();
       
```
