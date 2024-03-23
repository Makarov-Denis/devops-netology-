# devops-netology-
/terraform/.gitignore задаёт игнорирование следующих файлов, расположенных в директории "terraform" (файлы, расположенные вне иерархии этой директории, под влияние не попадают!):

Выражение .gitignore Действие
*/.terraform/ игнорировать всё содержимое иерархии папки с именем ".terraform" в какой бы глубине вложенности любых других директорий эта папка бы не находилась (таких папок может быть и несколько в различных иерархиях);
*.tfstate
*.tfvars

игнорировать все файлы с расширениями "tfstate" и "tfvars" где бы они ни находились;
.tfstate. игнорировать все файлы, в составе имени которых есть строка ".tfstate." где бы они ни находились. Например, будет проигнорирован файл(ы) "my.tfstate.txt";
crash.log
override.tf
override.tf.json
.terraformrc
terraform.rc игнорировать все файлы с указанными именами. В данном случае это файлы "crash.log", "override.tf", "override.tf.json", ".terraformrc" и "terraform.rc" независимо от их расположения;
*_override.tf
_override.tf.json игнорировать файлы, имена которых заканчиваются на указанные строки, например "myFile_override.tf" и "myFile_override.tf.json";

Если нужно отслеживать определенный файл в игнорируемой директории, то нужно указать путь к нему, предварив его восклицательным знаком. Например, нужно игнорировать всю директорию "myDir", кроме файла "myFile.txt" из неё:
myDir/
!myDir/myFile.txt
