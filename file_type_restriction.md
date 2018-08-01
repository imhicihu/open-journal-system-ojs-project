```
if (move_uploaded_file($_FILES[$fileName]['tmp_name'], $destFileName)){    
				
    			$allowed 	=   array('gif','png' ,'jpg', 'pdf', 'doc', 'docx'); // Type Extension
    			$filename 	=   $_FILES[$fileName]['name'];
    			$ext 		=   strtolower(pathinfo($filename, PATHINFO_EXTENSION));    
		
    			if(!in_array($ext,$allowed) ) {
    				return false;    				
    			}else{    				
    				return $this->setMode($destFileName, FILE_MODE_MASK);    				
    			}   		    			
}
```