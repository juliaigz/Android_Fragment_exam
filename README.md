# Android_Fragment_exam
### This is a project made in java and xml, using fragment and binding


![image](https://github.com/juliaigz/Android_Fragment_exam/assets/40221707/8fefe2b7-1104-47a7-a7af-67b975257713)

![image](https://github.com/juliaigz/Android_Fragment_exam/assets/40221707/1f9f2d10-2c36-46dd-8410-3cab359ff71d)


![image](https://github.com/juliaigz/Android_Fragment_exam/assets/40221707/07460aa2-9b5c-4677-911a-be20787e883e)


´´´bash
String phoneNumber = "1234567890"; // Número de teléfono al que deseas enviar un mensaje

                // Crea el URI con el número de teléfono en el formato adecuado
                Uri uri = Uri.parse("https://api.whatsapp.com/send?phone=" + phoneNumber);

                // Crea el intent con la acción ACTION_SEND y establece el URI
                Intent intent = new Intent(Intent.ACTION_SEND, uri);

                // Establece el tipo de contenido del mensaje como texto plano
                intent.setType("text/plain");

                // Verifica si WhatsApp está instalado en el dispositivo antes de iniciar la actividad
                PackageManager packageManager = getPackageManager();
                if (intent.resolveActivity(packageManager) != null) {
                    startActivity(intent);
                } else {
                    Toast.makeText(MainActivity2.this, "WhatsApp no está instalado", Toast.LENGTH_SHORT).show();
                }
 ´´´
