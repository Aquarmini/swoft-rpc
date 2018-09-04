# swoft-rpc

基本配置 app.php
~~~
return [
    ...
    'service' => [
        'default' => [
            'name' => 'service',
            'uri' => [
                '127.0.0.1:8099',
                '127.0.0.1:8099',
            ],
            'minActive' => 8,
            'maxActive' => 8,
            'maxWait' => 8,
            'maxWaitTime' => 3,
            'maxIdleTime' => 60,
            'timeout' => 8,
            'useProvider' => false,
            'balancer' => 'random',
            'provider' => 'consul',
        ]
    ],
    'breaker' => [
        'default' => [
            'failCount' => 3,
            'successCount' => 3,
            'delayTime' => 500,
        ],
    ],
    'provider' => require __DIR__ . DS . 'provider.php',
    'message' => require __DIR__ . DS . 'message.php',
    'queue' => require __DIR__ . DS . 'queue.php',
    'beanScan' => require __DIR__ . DS . 'beanScan.php',
    'components' => require __DIR__ . DS . 'components.php',
];
~~~
