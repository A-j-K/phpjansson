# PHP Jansson
A wrapper class for the Jansson C library.

The PHP class Jansson\Jansson is a wrapper around a JSON object key/value
store. Unlike PHP's json_encode() function Jansson\Jansson streams it's
encoded output direct to a PHP stream thus avoiding the memory consuming
process of converting a PHP array into a JSON string and then sending that
PHP string to output (which if output buffering is in use means sending a 
string memory buffer to yet another output memory buffer). Instead, the 
Jansson\Jansson class writes it's output chucked to the stream you specify.

Note, you need Jansson version 2.7 or greater to compile and use this wrapper.

https://github.com/akheron/jansson
http://jansson.readthedocs.org/en/latest

jansson.php is a "stub class" definition which provides the class method 
prototypes to assist your IDE in code completion, tooltips, etc.

See the tests/basic.phpt unit test file for instructions on how to use the PHP class.

    phpize
    ./configure --with-jansson
    make
    make install
    make test TESTS=.  [optional]

