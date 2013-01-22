# odisee-client-php

## Example

    // Create Odisee client with service URL and authentication
    $odisee = Odisee::createClient('http://service.odisee.de', 'username', 'password');
    // Create a new request for template HalloOdisee
    $request = $odisee->createRequest('HalloOdisee');
    // Set value for userfield 'hallo'
    $odisee->setUserfield($request, 'hallo', 'Odisee');
    // Set value in table 'Tabelle1' cell 'A4'
    $odisee->setTableCellValue($request, 'Tabelle1', 'A4', 'value in a table cell');
    // Generate document, PDF by default
    $document = $odisee->process();
