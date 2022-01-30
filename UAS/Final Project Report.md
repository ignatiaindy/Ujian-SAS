# Final Project Report

**From Group 6 [ IT 02-02 ]**

**Gede Reyki Astika   1202190052 || Ignatia Indreswari  1202190022**

------

## Step by Step

------

Scheme :

![00_scheme](D:\ITTelkom IT\SAS\UAS\assets\00_scheme.png)

------

Make new lxc and configure the IP of each lxc

![01_0_sudo_lxc_ls](D:\ITTelkom IT\SAS\UAS\assets\01_0_sudo_lxc_ls.PNG)

install open ssh server in all of the lxc above, after that we go to ansible

```
apt install openssh-server
```

Go to

```
cd ~/ansible/TUBES
```

And then go to 'nano hosts' to classified each lxc just like the scheme above

![01_1_nano_hosts](D:\ITTelkom IT\SAS\UAS\assets\01_1_nano_hosts.PNG)

And then

```
nano install-ci.yml //for code igniter
nano install-laravel.yml //for laravel
nano install-wp.yml //for wordpress
nano install-yii.yml //for yii2.0
nano install-mariadb.yml //for phpmyadmin
```

![01_2_tubes_ls](D:\ITTelkom IT\SAS\UAS\assets\01_2_tubes_ls.PNG)

![01_3_install_ci_yml](D:\ITTelkom IT\SAS\UAS\assets\01_3_install_ci_yml.PNG)

![01_4_install_laravel_yml](D:\ITTelkom IT\SAS\UAS\assets\01_4_install_laravel_yml.PNG)

![01_5_install_wp_yml](D:\ITTelkom IT\SAS\UAS\assets\01_5_install_wp_yml.PNG)

![01_6_install_yii_yml](D:\ITTelkom IT\SAS\UAS\assets\01_6_install_yii_yml.PNG)

![01_7_install_mariadb_yml](D:\ITTelkom IT\SAS\UAS\assets\01_7_install_mariadb_yml.PNG)

After all done we go to

```
cd /roles/ci/tasks
nano main.yml
```

![02_1_app_ci_tasks_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_1_app_ci_tasks_main_yml.PNG)

![02_2_app_ci_tasks_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_2_app_ci_tasks_main_yml.PNG)

![02_3_app_ci_tasks_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_3_app_ci_tasks_main_yml.PNG)

![02_4_app_ci_tasks_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_4_app_ci_tasks_main_yml.PNG)

After all done we go to

```
cd ../templates
nano app.conf
```

![02_5_app_ci_templates_app_conf](D:\ITTelkom IT\SAS\UAS\assets\02_5_app_ci_templates_app_conf.PNG)

After all done we go to

```
cd ../handlers
nano main.yml
```

![02_6_app_ci_handlers_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_6_app_ci_handlers_main_yml.PNG)

The ansible for Code Igniter is done, the we go to

```
cd ../../
cd php/tasks
nano main.yml
```

![02_7_php_tasks_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_7_php_tasks_main_yml.PNG)

![02_8_php_tasks_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_8_php_tasks_main_yml.PNG)

Then go to

```
cd ../handlers
nano main.yml
```

![02_9_php_handlers_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_9_php_handlers_main_yml.PNG)

The ansible for php is done, next one is Laravel, we need to go to

```
cd ../../
cd lv/tasks
nano main.yml
```

![02_10_lv_tasks_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_10_lv_tasks_main_yml.PNG)

![02_11_lv_tasks_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_11_lv_tasks_main_yml.PNG)

![02_12_lv_tasks_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_12_lv_tasks_main_yml.PNG)

After that we go to

```
cd ../templates
nano env.template
```

![02_13_lv_templates_env_template](D:\ITTelkom IT\SAS\UAS\assets\02_13_lv_templates_env_template.PNG)

![02_14_lv_templates_env_template](D:\ITTelkom IT\SAS\UAS\assets\02_14_lv_templates_env_template.PNG)

Then go to

```
nano lv.conf
```

![02_15_lv_templates_lv_conf](D:\ITTelkom IT\SAS\UAS\assets\02_15_lv_templates_lv_conf.PNG)

After configuring in templates, we go to handlers

```
cd ../handlers
nano main.yml
```

![02_16_lv_handlers_main.yml](D:\ITTelkom IT\SAS\UAS\assets\02_16_lv_handlers_main.yml.PNG)

The ansible for Laravel is done, the next one is mariadb, first we go to

```
cd ../../../
cd db/tasks
nano main.yml
```

![02_17_db_tasks_main.yml](D:\ITTelkom IT\SAS\UAS\assets\02_17_db_tasks_main.yml.PNG)

Then go to templates

```
cd ../templates
nano my.cnf
```

![02_18_db_templates_my_cnf](D:\ITTelkom IT\SAS\UAS\assets\02_18_db_templates_my_cnf.PNG)

Next go to handlers

```
cd ../handlers
nano main.yml
```

![02_19_db_handlers_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_19_db_handlers_main_yml.PNG)

The ansible for database is done, the next one is for PHP My Admin, just like before we need to go to

```
cd ../../
cd pma/tasks
nano main.yml
```

![02_20_pma_tasks_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_20_pma_tasks_main_yml.PNG)

![02_21_pma_tasks_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_21_pma_tasks_main_yml.PNG)

![02_23_pma_tasks_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_23_pma_tasks_main_yml.PNG)

Then go to

```
cd ../templates
nano lxc_mariadb.conf
```

![02_24_pma_templates_lxcmariadb_conf](D:\ITTelkom IT\SAS\UAS\assets\02_24_pma_templates_lxcmariadb_conf.PNG)

Then go to handlers

```
cd ../handlers
nano main.yml
```

![02_25_pma_handlers_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_25_pma_handlers_main_yml.PNG)

Yay the ansible for PHP My Admin is done, next one is YII2.0

```
cd ../../
cd yii/tasks
nano main.yml
```

![02_26_yii_tasks_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_26_yii_tasks_main_yml.PNG)

![02_27_yii_tasks_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_27_yii_tasks_main_yml.PNG)

![02_28_yii_tasks_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_28_yii_tasks_main_yml.PNG)

The next one we go to templates

```
cd ../templates
nano yii.conf
```

![02_29_yii_templates_yii_conf](D:\ITTelkom IT\SAS\UAS\assets\02_29_yii_templates_yii_conf.PNG)

![02_30_yii_templates_yii_conf](D:\ITTelkom IT\SAS\UAS\assets\02_30_yii_templates_yii_conf.PNG)

Then we go to handlers

```
cd ../handlers
nano main.yml
```

![02_31_yii_handlers_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_31_yii_handlers_main_yml.PNG)

The ansible for YII2.0 is done, so the next one is Wordpress

```
cd ../../
cd wp/tasks
nano main.yml
```

![02_32_wp_tasks_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_32_wp_tasks_main_yml.PNG)

Then go to templates

```
cd ../templates
nano wp.conf
```

![02_33_wp_templates_wp_conf](D:\ITTelkom IT\SAS\UAS\assets\02_33_wp_templates_wp_conf.PNG)

Then

```
nano wp.local
```

![02_34_wp_templates_wp_local](D:\ITTelkom IT\SAS\UAS\assets\02_34_wp_templates_wp_local.PNG)

Don't forget to go to handlers

```
cd ../handlers
nano main.yml
```

![02_35_wp_handlers_main_yml](D:\ITTelkom IT\SAS\UAS\assets\02_35_wp_handlers_main_yml.PNG)

This is the configuration for vm.local

```
sudo nano /etc/nginx/sites-available/vm.local
```

![02_36_etc_sites_availabe_vmlocal](D:\ITTelkom IT\SAS\UAS\assets\02_36_etc_sites_availabe_vmlocal.PNG)

![02_37_etc_sites_availabe_vmlocal](D:\ITTelkom IT\SAS\UAS\assets\02_37_etc_sites_availabe_vmlocal.PNG)

![02_38_etc_sites_availabe_vmlocal](D:\ITTelkom IT\SAS\UAS\assets\02_38_etc_sites_availabe_vmlocal.PNG)

This is the configuration for hosts in VM

```
nano /etc/hosts
```

![02_39_etc_hosts_vm](D:\ITTelkom IT\SAS\UAS\assets\02_39_etc_hosts_vm.PNG)

![03_1_ansibleplaybook_pma_mariadb](D:\ITTelkom IT\SAS\UAS\assets\03_1_ansibleplaybook_pma_mariadb.PNG)

After we add the ansible, then we run them using

```
ansible-playbook -i hosts install-''.yml -k
```

The first one is mariadb

![03_2_ansibleplaybook_pma_mariadb](D:\ITTelkom IT\SAS\UAS\assets\03_2_ansibleplaybook_pma_mariadb.PNG)

![03_3_ansibleplaybook_pma_mariadb](D:\ITTelkom IT\SAS\UAS\assets\03_3_ansibleplaybook_pma_mariadb.PNG)

Next is Laravel

![03_4_ansibleplaybook_laravel](D:\ITTelkom IT\SAS\UAS\assets\03_4_ansibleplaybook_laravel.PNG)

![03_5_ansibleplaybook_laravel](D:\ITTelkom IT\SAS\UAS\assets\03_5_ansibleplaybook_laravel.PNG)

The next one is Code Igniter

![03_8_ansibleplaybook_ci](D:\ITTelkom IT\SAS\UAS\assets\03_8_ansibleplaybook_ci.PNG)

![03_9_ansibleplaybook_ci](D:\ITTelkom IT\SAS\UAS\assets\03_9_ansibleplaybook_ci.PNG)

And then Wordpress

![03_10_ansibleplaybook_wp](D:\ITTelkom IT\SAS\UAS\assets\03_10_ansibleplaybook_wp.PNG)

![03_11_ansibleplaybook_wp](D:\ITTelkom IT\SAS\UAS\assets\03_11_ansibleplaybook_wp.PNG)

Then YII2.0

![03_12_ansibleplaybook_yii](D:\ITTelkom IT\SAS\UAS\assets\03_12_ansibleplaybook_yii.PNG)

![03_13_ansibleplaybook_yii](D:\ITTelkom IT\SAS\UAS\assets\03_13_ansibleplaybook_yii.PNG)

YAY

![04_1_notepad_host](D:\ITTelkom IT\SAS\UAS\assets\04_1_notepad_host.PNG)

The Result

![04_2_kelompok06_fpsas_app_ci](D:\ITTelkom IT\SAS\UAS\assets\04_2_kelompok06_fpsas_app_ci.PNG)

![04_3_kelompok06_fpsas_product_yii](D:\ITTelkom IT\SAS\UAS\assets\04_3_kelompok06_fpsas_product_yii.PNG)

![04_4_news_kelompok06_fpsas_wp](D:\ITTelkom IT\SAS\UAS\assets\04_4_news_kelompok06_fpsas_wp.PNG)

![04_5_news_kelompok06_fpsas_wp_sukese](D:\ITTelkom IT\SAS\UAS\assets\04_5_news_kelompok06_fpsas_wp_sukese.PNG)

![04_6_news_kelompok06_fpsas_wp_masok](D:\ITTelkom IT\SAS\UAS\assets\04_6_news_kelompok06_fpsas_wp_masok.PNG)

![04_7_news_kelompok06_fpsas_wp_helloworld](D:\ITTelkom IT\SAS\UAS\assets\04_7_news_kelompok06_fpsas_wp_helloworld.PNG)

![04_8_kelompok06_fpsas_laravel](D:\ITTelkom IT\SAS\UAS\assets\04_8_kelompok06_fpsas_laravel.PNG)

![04_9_kelompok06_fpsas_phpmyadmin](D:\ITTelkom IT\SAS\UAS\assets\04_9_kelompok06_fpsas_phpmyadmin.PNG)

![04_10_kelompok06_fpsas_phpmyadmin](D:\ITTelkom IT\SAS\UAS\assets\04_10_kelompok06_fpsas_phpmyadmin.PNG)

------

JMeter

Using load balancer

50

Landing : 757
Blog : 793
App : 675
Product : 347

![05_1_jmeter_50_sumreport](D:\ITTelkom IT\SAS\UAS\assets\05_1_jmeter_50_sumreport.PNG)

150

Landing : 710
Blog : 524
App : 407
Product : 256

![05_2_jmeter_150_sumreport](D:\ITTelkom IT\SAS\UAS\assets\05_2_jmeter_150_sumreport.PNG)

300

Landing : 631
Blog : 143
App : 154
Product : 171

![05_3_jmeter_300_sumreport](D:\ITTelkom IT\SAS\UAS\assets\05_3_jmeter_300_sumreport.PNG)

500

Landing : 528
Blog : 154
App : 181
Product : 181

![05_4_jmeter_500_sumreport](D:\ITTelkom IT\SAS\UAS\assets\05_4_jmeter_500_sumreport.PNG)

Not using load balancer

50

Landing : 43
Blog : 12
App : 16
Product : 18

![05_5_jmeter_50_before](D:\ITTelkom IT\SAS\UAS\assets\05_5_jmeter_50_before.PNG)

150

Landing : 36
Blog : 11
App : 12
Product : 7

![05_6_jmeter_150_before](D:\ITTelkom IT\SAS\UAS\assets\05_6_jmeter_150_before.PNG)

300

Landing : 38
Blog : 11
App : 12
Product : 7

![05_7_jmeter_300_before](D:\ITTelkom IT\SAS\UAS\assets\05_7_jmeter_300_before.PNG)

500

Landing : 47
Blog : 15
App : 15
Product : 9

![05_8_jmeter_500_before](D:\ITTelkom IT\SAS\UAS\assets\05_8_jmeter_500_before.PNG)

------

Analysis

Below is the results from when we use load balancer

 - When there is 50 users that access our web, if we use load balancer then the average throughput is
   - landing : 757 s
   - blog : 793 s
   - app : 675 s
   - product : 347 s
- When there is 150 users, then
  - landing : 710 s
   - blog : 524 s
   - app : 407 s
   - product : 256 s
- When there is 300 users, then
  - landing : 631 s
  - blog : 143 s
  - app : 154 s
  - product : 171 s
- When there is 500 users, then
  - landing : 528 s
  - blog : 154 s
  - app : 181 s
  - product : 181 s
- When there is 50 users that access our web, if we use load balancer then the number of user accessing our web is
  - landing : 757 user /s
  - blog : 793 user /s
  - app : 675 user /s
  - product : 347 user /s
- When there is 150 users, then
  - landing : 710 user /s
  - blog : 524 user /s
  - app : 407 user /s
  - product : 256 user /s
- When there is 300 users, then
  - landing : 631 user /s
  - blog : 143 user /s
  - app : 154 user /s
  - product : 171 user /s
- When there is 500 users, then
  - landing : 528 user /s
  - blog : 154 user /s
  - app : 181 user /s
  - product : 181 user /s

With changing load balancer method so that we can get the best performance, we think using Weighted Load Balancing is bringing our web to its best performance

There are some factors too

- The number of user accessing our web

  When the number of user accessing our web is high, then automatically the troughput and the number of user that can access the web become lesser

- Insufficient bandwidth server

  Just like bandwidth server, the larger the bandwidth is then the number of user that can access the web is larger too

- Using the wrong load balancer method

  The use of load balancer is greatly affects user access to the web, if we use the wrong load balancer, it will take a lot of time for the users to access our web, which affects the number of user accessing it

------

## Thank You