# twitter api notes
 twitter api notes
 
 Twitter ID and username converter
 https://tweeterid.com/
 
 twitter url redirect user id to username
 https://twitter.com/intent/user?user_id=382247773
 
 
 -----------------------------
 v2 API and the bearer token (bearer token is some kind of simplified method to access public data through an OAuth 2.0 API)

$authorization = "Authorization: Bearer YOUREXTRALONGBEARERYOUREXTRALONGBEARERYOUREXTRALONGBEARERYOUREXTRALONGBEARERYOUREXTRALONGBEARERYOUREXTRALONGBEAR";
$ch = curl_init();
curl_setopt($ch, CURLOPT_HTTPHEADER, array('Content-Type: application/json', $authorization));
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_setopt($ch, CURLOPT_URL, "https://api.twitter.com/2/users/by/username/TwitterFrance?user.fields=public_metrics");
$result = curl_exec($ch);
curl_close($ch);
if (is_string($result)) {
    echo (json_decode($result)->data->public_metrics->followers_count);
    die();
}
 
 --------------


.enhanced-mini-profile .mini-profile .profile-summary {
  background-image: url(https://pbs.twimg.com/profile_banners/2622731/1401943819/mobile);
}
The number after profile_banners/ is the account's Twitter user ID, which won't change if the account's screen name is changed. Here, 2622731 is my personal Twitter ID. (Expect to see much later numbers for more recent accounts; mine is quite old.)


-------------------
