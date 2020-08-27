# PatientModel

  ##  public function get_login_info($data)
    {
        if($data['lan'] == 'en'){
            $query = $this->db->query("SELECT * from `user_details` where `user_email`='".$data['Mobile']."' && `user_password`='".$data['Password']."'");
        }elseif($data['lan'] == 'vn'){
            $query = $this->db->query("SELECT * from `ln_user_details` where `user_email`='".$data['Mobile']."' && `user_password`='".$data['Password']."'");
        }
        if($query->num_rows()==1)
        {
            return true;
            exit;
        }
        return false;
    }
