# Winhttpclient-c
Winhttpclient is an interface which packaged with WinHTTP API written in c. And thanks  Brian Lyttle a lot.

the main interface:
    int SendHttpRequest(const wchar_t *verb, wchar_t *url, unsigned char *sendbuf,int sendbuflen, char *output,BOOL proxyFlah);
    
    verb: GET or POST
    url : http and https are both supported.
    output: the responsed data from server is stored in output.
    proxyFlag: Sending message with proxy or not.

# To compile with gcc:
    
    
    gcc test.c winhttpclient.c -o test.exe -l winhttp
        \____/ \_____________/  \________/  \________/
          |           |             |           |
   Your own source    |           Output        |
                      |                  Link winhtttp lib
           Link winhttpclient.c
