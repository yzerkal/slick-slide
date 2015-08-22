This repository is the copy of DrMabuse23/yii2-slick except of hardcoded slick-slide version in composer.json

yii2-slick
==========

[the Preview http://kenwheeler.github.io/slick/](http://kenwheeler.github.io/slick/ "http://kenwheeler.github.io/slick/")

The yii2 widget to the fantastic slick-carousel. This widget generate you the only the javascript.

###Installation Composer
    yzerkal/slick-slide:"*"

### Installation Assets Bower
    cd vendor/yzerkal/slick-slide/web

    bower install

###Using

~~~

	\drmabuse\slick\SlickWidget::widget([
		'container' => '.single-item',
		'settings'  => [
			'slick' => [
				'infinite'      =>  true,
				'slidesToShow'  =>  3,
				'onBeforeChange'=> new \yii\web\JsExpression('function(){
				}'),
				'onAfterChange' => new \yii\web\JsExpression('function(){
					console.debug(this);
				}'),
				'responsive' => [
					[
						'breakpoint'=> 768,
						  'settings'=> [
							  'arrows'=> false,
							  'centerMode'=> true,
							  'centerPadding'=> 40,
							  'slidesToShow'=> 3
						  ]
					]
				],
			],
			'slickGoTo'         => 3,
		]
	]);

    <div class="slider single-item">
        <div><h3>1</h3></div>
        <div><h3>2</h3></div>
        <div><h3>3</h3></div>
        <div><h3>4</h3></div>
        <div><h3>5</h3></div>
        <div><h3>6</h3></div>
    </div>

~~~
