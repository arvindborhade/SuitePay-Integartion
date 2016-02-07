# SuitePay-Integartion
Suite Pay CI integration Library 

Add library at application/config/autoload.php 
$autoload['libraries'] = ('suitepay');

    $mid = "99";   // this changes to live mid after testing period
		$creditcard = "4660840000058018";
		$month = "09";  // MM
		$year = "18";     // YY - remeber 2 digits
		$cvv = "111";
		$amount = "129.23";			
		$ch_name="John Smith";
		$opt = "";
		
		$baddress="123 some st";
		$baddress2="apt 1";
		$bcity="Beverly Hills";
		$bcountry="US";   
		$bstate="CA";
		$bzip="90210";
		$cphone="1234567890";
		$ipaddress="0.0.0.0";
		$cfirstname="John";
		$clastname="Smith";
		$currency= 'USD';
		$cemail="test@test.com";
		$cwebaddress="www.web.com";
				 

		$credit_card = array(
						'mid'=>$mid,
						'amount' => $amount,
						'creditcard' => $creditcard,
						'cardfullname' => $ch_name,
						'cvv' => $cvv,
						'currency' => 'USD',
						'month' => $month,
						'year' => $year, 
		);
		
		$customer = array(		   
				   'baddress' => $baddress,
				   'bcountry' => $bcountry,
				   'bcity' => $bcity,
				   'bstate' => $bstate,
				   'bzip' => $bzip,
				   'cfirstname' => $cfirstname,
				   'clastname' => $clastname,
				   'cphone' => $cphone,
				   'cemail' => $cemail,
                   'ipaddress' => $ipaddress,
		);		
		$client_id = "12";
		$order_id = "12";

		$this->suitepay->Charge($client_id, $order_id, $customer, $amount, $credit_card);
