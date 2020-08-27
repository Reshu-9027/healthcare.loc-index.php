# Replace this function  

public function regi_login()
    {
        $inputdata=json_decode(file_get_contents("php://input"), true);
        
        $logindata['login']=$this->patientmodel->get_login_info($inputdata);
        
        if ($logindata['login']==true) 
        {
            $mdata=$this->patientmodel->get_user_databyemail($inputdata['Mobile']);
            $response = array(
                'status' => true,
                'message' => 'Login successful',
                'data'=>$mdata
                );
        }
        else
        {
            $response = array(
                'status' => false,
                'message' => 'UserName & password Not Found'
                );
        }
        echo json_encode($response);   

    }
    
    # note change input type="text" to type="email" in login_en  && login_vn
