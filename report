import os
import time
import pywhatkit as kit

# Definiciones de variables (asegúrate de definir estas en tu código)
C = "\033[0m"  # Color por defecto
G = "\033[92m"  # Verde
R = "\033[91m"  # Rojo
wp = ""  # Aquí puedes definir el valor de wp
title = {
    'title9': 'Título para Retirar Banimento 1',
    'title10': 'Título para Retirar Banimento 2',
    'title11': 'Título para Banir Número 1',
    'title12': 'Título para Banir Número 2',
    'title13': 'Título para Derrubar Blindagem',
    'title14': 'Título para Blindar Número 1',
    'title15': 'Título para Blindar Número 2'
}
text = {
    'text9': 'Contenido para Retirar Banimento 1',
    'text10': 'Contenido para Retirar Banimento 2',
    'text11': 'Contenido para Banir Número 1',
    'text12': 'Contenido para Banir Número 2',
    'text13': 'Contenido para Derrubar Blindagem',
    'text14': 'Contenido para Blindar Número 1',
    'text15': 'Contenido para Blindar Número 2'
}

def clear():
    os.system('clear' if os.name == 'posix' else 'cls')

def send_whatsapp_report(titulo, bd, phone_number):
    try:
        # Enviar mensaje a través de WhatsApp
        kit.sendwhatmsg_instantly(phone_number, f'Título: {titulo}\nContenido: {bd}')
        print("Reporte enviado por WhatsApp exitosamente.")
    except Exception as e:
        print(f"Ocurrió un error al enviar el reporte por WhatsApp: {e}")

def report_and_suspend_number(phone_number_to_report):
    message = f"Hola soporte de WhatsApp,\n\nQuiero reportar y solicitar la suspensión del siguiente número: {phone_number_to_report}.\nPor favor, tomen las medidas necesarias.\n\nGracias."
    
    try:
        kit.sendwhatmsg_instantly("+14155238886", message)  # Reemplaza con el número oficial de soporte si es necesario
        print("Número reportado y solicitado suspensión al soporte de WhatsApp exitosamente.")
    except Exception as e:
        print(f"Ocurrió un error al enviar el reporte al soporte: {e}")

def send_report(titulo, bd, phone_number):
    print(f"Enviando reporte:\nTítulo: {titulo}\nContenido: {bd}")
    
    # Exportar el reporte a un archivo
    export_report(titulo, bd)
    
    # Enviar el reporte por WhatsApp
    send_whatsapp_report(titulo, bd, phone_number)

def export_report(titulo, bd):
    with open('reporte.txt', 'a') as f:
        f.write(f'Título: {titulo}\nContenido: {bd}\n\n')

def init():
    print("Inicializando...")  # Mensaje de inicialización

def main():
    Sair = False
    phone_number = "+57XXXXXXXXXX"  # Reemplaza con el número de teléfono de destino en formato internacional
    while not Sair:
        try:
            op = int(input("Seleccione una opción: "))
            if op == 3:
                clear()
                op2 = int(input("Seleccione una subopción: "))
                if op2 == 1:
                    clear()
                    print(wp, f'{C}Modo:{G} Retirar Banimento{C}\n')
                    titulo = title['title9']
                    bd = text['text9']
                    send_report(titulo, bd, phone_number)
                elif op2 == 2:
                    clear()
                    print(wp, f'{C}Modo:{G} Retirar Banimento{C}\n')
                    titulo = title['title10']
                    bd = text['text10']
                    send_report(titulo, bd, phone_number)
                init()
            elif op == 4:
                clear()
                op2 = int(input("Seleccione una subopción: "))
                if op2 == 1:
                    clear()
                    print(wp, f'{C}Modo:{R} Banir Número{C}\n')
                    titulo = title['title11']
                    bd = text['text11']
                    send_report(titulo, bd, phone_number)
                elif op2 == 2:
                    clear()
                    print(wp, f'{C}Modo:{R} Banir Número{C}\n')
                    titulo = title['title12']
                    bd = text['text12']
                    send_report(titulo, bd, phone_number)
                init()
            elif op == 5:
                clear()
                print(wp, f'{C}Modo:{R} Derrubar Blindagem{C}\n')
                titulo = title['title13']
                bd = text['text13']
                send_report(titulo, bd, phone_number)
            elif op == 6:
                clear()
                op2 = int(input("Seleccione una subopción: "))
                if op2 == 1:
                    clear()
                    print(wp, f'{C}Modo:{G} Blindar Número{C}\n')
                    titulo = title['title14']
                    bd = text['text14']
                    send_report(titulo, bd, phone_number)
                elif op2 == 2:
                    clear()
                    print(wp, f'{C}Modo:{G} Blindar Número{C}\n')
                    titulo = title['title15']
                    bd = text['text15']
                    send_report(titulo, bd, phone_number)
                init()
            elif op == 7:
                while True:
                    os.fork()  # Ten cuidado con esto; puede causar un bucle infinito.
            elif op == 8:
                number_to_report = input("Ingrese el número que desea reportar (formato internacional): ")
                report_and_suspend_number(number_to_report)
            elif op in [9]:
                link()  # Asegúrate de definir esta función.
            elif op == 0:
                Sair = True
            else:
                print("Opción no válida.")
        except Exception as error:
            clear()
            print(f"Ocurrió un error: {error}")
            time.sleep(4)

if __name__ == "__main__":
    main()

# Limpieza final del sistema
os.system('rm -rf __pycache__ && '+clean) 
