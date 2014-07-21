// Google Script Custom Function to associate an individual contact with an existing deal in Base CRM
// 05/19/2014 by Vance Faulkner
 
 
function base_contact_to_deal(contact_id, deal_id) {
  var headers = {
    'X-Pipejump-Auth': '[YOUR TOKEN HERE]',
  };
  var url = 'https://sales.futuresimple.com/api/v1/deals/' + deal_id + '/contacts.json';
  var payload = '{"contact_id": "' + contact_id + '"}';
  var options = {
    'method': 'POST',
    'headers': headers,
    'contentType' : 'application/json',
    'payload': payload,
  };
  var response = UrlFetchApp.fetch(url, options);
  Logger.log(response);
  return response.getContentText()
}
