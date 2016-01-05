# Verysimple Unit Test Printer

PHPUnit ResultPrinter implementation that outputs verbose test information. Rather than see a string of dots and letters, this unit test printer will display the name of the suite and tests and number of assertions. If you manually run your tests and watch then running, you can more easily see the progress of your tests.

![](https://raw.githubusercontent.com/verysimple/unit-test-printer/master/assets/images/screenshot.jpg)

## Installation

Install VerboseTestResultPrinter class with composer:

	composer require verysimple/unit-test-printer

For automatic installation, include the project in your composer.json (it is only necessary in require-dev):

	{
		"require-dev": {
			"verysimple/unit-test-printer": ">=1.0.1"
		}
	}

If you do not use composer, you can download and save `VerboseTestResultPrinter.php` wherever you wish.

## Usage

To use the `VerboseTestResultPrinter` class, it is specified in your `phpunit.xml` config file. The following assumes `phpunit.xml` is in your project root directory and your tests are located in a sub-directory named "tests".

	<phpunit
		colors="true"
		printerClass="Verysimple\UnitTest\VerboseTestResultPrinter"
		printerFile="vendor/autoload.php"
		>
	
		<testsuite name="Default Tests">
			<directory>tests/</directory>
		</testsuite>
	
	</phpunit>

Alternatively you can add simply make sure the library is included in your test runner. For example, adding the following to your `phpunit_bootstrap.php file`:

	require __DIR__.'/vendor/autoload.php';

To run unit tests, execute phpunit from the root directory of the project.