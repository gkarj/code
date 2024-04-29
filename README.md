https://github.com/neo4j-contrib/spatial/releases

https://codingxpert.com/courses/ios-application-development/lessons/how-to-pass-data-from-one-viewcontroller-to-another-view-controller-in-swift/


segue : 
  @IBAction func btnSubmitClick(_ sender: Any) {
        self.performSegue(withIdentifier: "vc2", sender: self)
    }
    
    override func prepare(for segue: UIStoryboardSegue, sender: Any?) {
        if segue.identifier == "vc2"{
            if let vc = segue.destination as? SecondVC{
                vc.name = txtName.text!
                vc.email = txtEmail.text!
            }
        }
    }
