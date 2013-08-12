Using.js is a simple asynchronous script dependency loader for web browsers that allows a developer to write blocks of code in this fashion:

    // register in a preceding script ..
    using.register("jquery", true, "http://cachefile.net/scripts/jquery-1.2.3.js"); 
    
.. then consume synchronously .. 

    using("jquery"); // synchronously loads jQuery and de-registers jQuery from using 
    $("a").css("text-decoration", "none");

.. or asynchronously ..

    using ('jquery', function() {
        // do work using jQuery constructs
    });


It documents dependencies within script and alleviates the need for fussing with injecting script dependencies on specific page headers. It also supports dependency trees, i.e. `using('jquery-ui' ...)` might depend upon jQuery, which would be loaded first.

Similar loaders exist such as RequireJS. I am not antagonistic towards those, use what you please, but I chose the name, syntax, and behavior of using.js because it has some level of parallel to coding conventions in other languages such as C#.

For more information about how to use using.js, please view the history in [the Wiki](https://github.com/stimpy77/using.js/wiki).
