## Some useful commands  
  
### Download source rpm  
yumdownloader --source **package-name**  
  
### Rebuild from source rpm  
rpmbuild --rebuild **package-name**.src.rpm  
  
### Build from spec file  
rpmbuild --bb ~/rpmbuild/SPECS/**package-name**.spec  
  
### Build without debuginfo  
rpmbuild --rebuild --define "debug_package %{nil}" **package-name**.src.rpm  
rpmbuild --bb --define "debug_package %{nil}" ~/rpmbuild/SPECS/**package-name**.spec  
  
### Modify binary rpm  
export VISUAL=kwrite  
rpmrebuild -enp **package-name**.rpm  

### Build 32bit rpm  
setarch i386  
