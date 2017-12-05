<?php
//coded by pak haxor
Class Algorthm{
	private $tmp=array();
	private $STDIN = array();
	function __construct() {
		if(function_exists($this->execute())){
			$this->execute();
		}
	}
	private function CommandSTDIN($text){
		echo $text;
		$STDIN = trim(fgets(STDIN));
		return $STDIN;
	}
	private function update_last(&$array, $value){
	    array_pop($array);
	    array_push($array, $value);     
	}
	private function mathplus(){
		$this->STDIN = array_unique($this->STDIN);
		$this->tmp['result'] = array_sum($this->STDIN);
		if($this->tmp['result'] > $this->tmp['num']){
			return true;
		}
		return false;
	}
	private function loopSTDIN($loop = false){
		while (1 <= 100000) {
			$STDIN = $this->CommandSTDIN('Input Number For Algorthm (example : 1 or 0 Press Enter to finish) : ');
			if($STDIN == 0){
				if($this->tmp['result'] == 0){
					die("Ended..\n");
				}
				echo $this->algoritm1();
				exit;
			}elseif(in_array($STDIN, $this->STDIN)){
				echo "Warning : Already exist number \n";
				$this->loopSTDIN();
			}elseif($this->tmp['num']<=$STDIN){
				echo "Warning : Must be used Low numbered \n";
				$this->loopSTDIN();
			}
			else{ 
			$this->STDIN[] = $STDIN;
				if($this->mathplus()==true){
					echo "Warning : Calculation is ready \n";
					echo $this->algoritm1();
				exit;
				}
			}
		}
	}
	private function algoritm1(){
		sort($this->STDIN);
		$num = $this->tmp['num'];
		$this->algoritm2();
		if(empty($this->tmp['plus'])){
			echo 'Something error'; 
		}
		else{
		echo "Result : ".$this->tmp['plus']." = ".$this->tmp['num'];
		}
	}
	private function pressure(){
		foreach($this->STDIN as $pressure){
			if($this->tmp['sum']-$pressure==$this->tmp['num']){
				return $pressure;
			}
		}
	}
	private function algoritm2(){
		foreach($this->STDIN as $nums){
			$this->tmp['nums'][rand(5, 1000)] = $nums;
			if($this->tmp['sum']<$this->tmp['num']){
				$this->tmp['sum'] = array_sum($this->tmp['nums']);
				if($this->tmp['sum'] == $this->tmp['num']){
					$this->tmp['plus'] = implode('+',$this->tmp['nums']);
				}
			}
		}
		if($this->tmp['sum']>$this->tmp['num']) {
			$this->update_last($this->tmp['nums'],$this->pressure());
			if(array_sum($this->tmp['nums'])==$this->tmp['num']){
			$this->tmp['plus'] = implode('+',$this->tmp['nums']);
			}
		}
		if($this->tmp['sum']<$this->tmp['num']) $this->algoritm2();
	}
	private function execute(){
		$number = $this->CommandSTDIN('Input Your Number (example : 1) : ');
		if($number<=1) die("Don't Used 1 number Must High Numbers");
		if(!(int)$number) die("Wrong Input Please Using Number\n");
		$this->tmp['num'] = $number;
		$this->tmp['result'] = 0;
		$this->tmp['sum'] = 0;
		$this->loopSTDIN();
	}
}
new Algorthm;
