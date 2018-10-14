# PHP Language Server

Run as a docker image:

    docker run -p 127.0.0.1:2088:2088/tcp felixfbecker/php-language-server

Then set up in `init.vim`:

    " Language Client
    let g:LanguageClient_serverCommands = {
        \ 'php': ['tcp://127.0.0.1:2088'],
    \ }

