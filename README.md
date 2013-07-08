# ABO generator for PHP

	$abo = new abo();
	$abo->setComittentNumer(222780978);
	$abo->setOrganization("Ceska nar.zdrav.poj.");
	$abo->setDate('271198');
	$abo->setSecurityKey('123456', '654321');
	$account = $abo->addAccountFile(abo_account_file::INKASO);
	$account->setBank('0300'); //ktera banka bude zpracovavat, ta nase
	$account->setBankDepartment('82');
	$group = $account->addGroup();
	$group->setAccount(122780922);
	$group->setDate('271198');
	$group->addItem("174-1999738514/0300", 2000.5, 2220009813)
		->setConstSym('8')
		->setSpecSym('93653')
		->setMessage('první  èást');

	$group->addItem("5152046/0300", 2000, 2220000598)
		->setConstSym('8')
		->setSpecSym('93654');

	$group->addItem("192359658/0300", 2000, 2220000004)
		->setConstSym('8')		
		->setSpecSym('93655');
		

	$group->addItem("174-0346006514/0300", 2000, 2220497222)
		->setConstSym('8')
		->setSpecSym('93656')
		->setMessage('první  èást');
		
	$group->addItem("492732514/0300", 2000, 2220000811)
		->setConstSym('8')
		->setSpecSym('93657');



		echo '<pre>'.$abo->generate().'</pre>';

