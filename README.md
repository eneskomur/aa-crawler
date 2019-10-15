# Anadolu Ajansi News Crawler - Anadolu Ajansı Haber Robotu

[EN] This package is created for crawling news from Anadolu Ajansi. You have to be subscribed to AA and obtain user credentials for being able to use this package.

[TR] Bu paket AA abonelerinin kullanıcı bilgileriyle haberleri taramaları için oluşturulmuştur. Aşağıdaki şekilde kullandığınızda son eklenen haberlerden istediğiniz adette haberi dizi olarak alabilirsiniz. Paketi kullanmak için AA abonesi olmalı ve kullanıcı bilgilerine sahip olmalısınız.





## Install

Via Composer

``` bash
$ composer require eneskomur/aa-crawler
```

## Usage

``` php
$crawler = new \eneskomur\Agency\Aa\Crawler([
    'user_name' => 'your-username',
    'password' => 'your-password'
]);

$news = $crawler->crawl([
    'limit' => 10, //optional
]);
```
Calling `$crawler->crawl()` will return an array like this:

```php
[{
		"code": "aa:text:20170831:12935896",
		"title": "Title of the news 1",
		"summary": "Summary...",
		"content": "Content 1",
		"created_at": "31.08.2017 15:56:12",
		"category": "Genel",
		"city": "Istanbul",
		"images": ["http:\/\/path\/to\/news1\/image1", "http:\/\/path\/to\/news1\/image2"],
                "videos": ["http:\/\/path\/to\/news1\/video1", "http:\/\/path\/to\/news1\/video2"]
	},
	{
		"code": "aa:text:20170831:12935899",
		"title": "Title of the news 2",
		"summary": "Summary...",
		"content": "Content 2",
		"created_at": "31.08.2017 15:56:12",
		"category": "Genel",
		"city": "Ankara",
		"images": ["http:\/\/path\/to\/news2\/image1", "http:\/\/path\/to\/news2\/image2"],
                "videos": ["http:\/\/path\/to\/news2\/video1", "http:\/\/path\/to\/news2\/video2"]
	}
]
```
## Change log

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Testing

``` bash
$ composer test
```

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## Security

If you discover any security related issues, please email eneskomur@gmail.com instead of using the issue tracker.

## Credits

- [Yavuz Selim Bilgin][link-ysb]
- [Murat Paksoy][link-mp]
- [Enes Kömür][link-ek]
- [All Contributors][link-contributors]

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[link-ysb]: https://github.com/ysb
[link-mp]: https://github.com/slavesoul
[link-ek]: https://github.com/eneskomur
[link-contributors]: ../../contributors
