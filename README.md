# phpmysqlidump
Libreria para obtener un dump de mysql usando mysqli

La libreria original fue creada por awan < nawa (at) yahoo (dot) com, pero no he encontrado repositorio para hacer el fork
y encontré el php navegando hace tiempo.


Ejemplo de uso

require_once("phpmysqlidump.pclass");
$filename = "backup-" . date("YmdHi") . "";
$extension=".sql.gz";

backup_database( "database", $filename, $DBHOST, $DBUSER, $DBPASSWD, $DATABASE,array("log"),true); // execute
$salida=file_exists("database/".$filename.$extension);
if ($salida){
    echo "Se ha generado el fichero";
}else{
    echo "No se ha generado el fichero";
}
