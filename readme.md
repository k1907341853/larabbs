

运行 Laravel Mix: npm run watch-poll




计划任务：
    * * * * * php /Users/wangkai/web/larabbs/artisan schedule:run >> /dev/null 2>&1


用户最后登录时间 redis同步到数据库命令：
    手动同步：
        $ php artisan larabbs:sync-user-actived-at
        
    任务调度 app/Console/Kernel.php：
        // 每日零时执行一次
        $schedule->command('larabbs:sync-user-actived-at')->dailyAt('00:00');
    
        