Using.js is a simple, very lightweight asynchronous script dependency loader for web browsers that I wrote in 2008 that allows a developer to write blocks of code in this fashion:

    using("jquery"); // synchronously loads jQuery and de-registers jQuery from using 
    $("a").css("text-decoration", "none");

.. or asynchronously ..

    using ('jquery', function() {
        // do work using jQuery constructs
    });

It documents dependencies within script and alleviates the need for fussing with injecting script dependencies on specific page headers. It also supports dependency trees, i.e. `using('jquery-ui' ...)` might depend upon jQuery, which would be loaded first.

Similar loaders exist such as RequireJS. I am not antagonistic towards those, use what you please, but I chose the name, syntax, and behavior of using.js because it has some level of parallel to my coding styles in C#.

For more information about how to use using.js, please view the history in the Wiki.