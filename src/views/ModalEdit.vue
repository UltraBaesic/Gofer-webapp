


<template>
  <div>
    <div class="modal-content modal fade"  id="ModalEdit">
              <div class="modal-header">
                  <button type="button" class="close shadow-sm" data-dismiss="modal">&times;</button>
              </div>
              <div>
                  <p class="modal-text text-center font-weight-bold">Edit Profile</p>
              </div>
              <div class="verify-msg text-center p-4">
                <div class="user-picture">
                    <div class="pix-wrapper">
                        <img class="dash-profile" src="@/assets/img/profile.png" alt="">
                        <i class="material-icons verified-logo mr-2">edit</i></div>
                </div>
                <div class="form-group text-left">
                    <label for="" class="text-dark pt-0 pb-0">Name: </label>
                    <input type="text" class="form-control form-control-lg mb-1" value="" placeholder="Steven"
                        name="text1"><label for="" class="text-dark pt-0 pb-0">Email: </label>
                    <input type="text" class="form-control form-control-lg mb-1" value="" placeholder="steven.peters@gmail.com"
                        name="text1"><label for="" class="text-dark pt-0 pb-0">Phone No: </label>
                    <input type="text" class="form-control form-control-lg mb-1" value="" placeholder="08023456789"
                        name="text1">
                </div>
                <div class="mt-3">
                    <a class="btn mt3 btn-lg btn-primary px-5 pointer text-white">Submit</a>
                </div>
              </div>
            </div>
  </div>
</template>