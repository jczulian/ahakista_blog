
$arr['text'][6]['text'] = "Beauftragte(r)";
$data['sap_contractor'] = $arr;

$arr['text'][6]['text'] = "Ihre Emailadresse:";
$data['yourEmail'] = $arr;

$arr['text'][6]['text'] = "Zur Zeit sind keine Mandate geplant. Bitte schauen sie später wieder vorbei.";
$arr['text'][1]['text'] = "Currently no mandates are planned, please check again later.";
$data['sap_contract_noentries'] = $arr;

$cs = new commonStrings();
$cs->addCommonStrings($data);
