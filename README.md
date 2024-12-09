# ContrataChain Frontend: Plataforma de Calificación de Proveedores

<h4 align="center">
  <a href="https://github.com/contratachain/">Documentación más general</a>
  <a href="https://github.com/contratachain/contratachainFrontend">Documentación Frontend (este mismo repositorio)</a>
</h4>

Bienvenido al frontend de **ContrataChain**, una plataforma descentralizada que utiliza **blockchain** para garantizar la transparencia en la calificación y contratación de proveedores en Colombia. Esta plataforma tiene como objetivo reducir la corrupción y mejorar la eficiencia en la contratación pública y privada. Por ahora es en Colombia, pero se puede expandir a todos los paises latinoamericanos. Casi que todos los paises tienen el mismo modus operandi.

## Descripción del Proyecto

La plataforma *ContrataChain* permite la evaluación, calificación y seguimiento de proveedores a través de la tecnología **blockchain**. Los proveedores registrados son evaluados en función de su historial de cumplimiento, la calidad de sus productos o servicios, y su desempeño en contratos previos. Mediante el uso de **smart contracts**, todo el proceso es transparente, seguro e inmutable.

Los principales usuarios de la plataforma son empresas y organismos gubernamentales que buscan tomar decisiones informadas al contratar proveedores, reduciendo así los riesgos asociados con la corrupción y la falta de transparencia.

Este proyecto está basado en **Scaffold-ETH 2**, **Next.js** para la interfaz frontend y **Hardhat** para el desarrollo de contratos inteligentes.

## Funcionalidades que se supone que debía hacer (pero no hice por estar tomando el día de velitas en colombia, nunca volveré a participar en hackatones durante epocas decembrinas)

### Características Principales:
- **Visualización de Calificaciones**: Los usuarios pueden consultar las calificaciones y la información detallada de los proveedores registrados.
- **Interfaz Intuitiva**: La plataforma cuenta con una interfaz fácil de usar, diseñada para facilitar la búsqueda y evaluación de proveedores.
- **Integración con Secop II**: Acceso a información de proveedores registrados en el sistema estatal de contratación pública, esto a través de la API que de socrata/python que ellos internamente utilizan.  
- **Blockchain**: Toda la información relacionada con los proveedores y sus calificaciones está almacenada de forma segura en la blockchain, garantizando la inmutabilidad de los datos.

## Tecnologías Utilizadas

El frontend de la plataforma está desarrollado con las siguientes tecnologías:

- **Scaffold-ETH 2**: Framework que facilita el desarrollo rápido de aplicaciones descentralizadas sobre Ethereum, usando Hardhat y Next.js.
- **Next.js**: Framework basado en React para la creación de interfaces web modernas y escalables.
- **Hardhat**: Entorno de desarrollo para contratos inteligentes, utilizado para compilar, probar e implementar contratos en Ethereum.
- **Solidity**: Lenguaje de programación que entiende la EVM.
- **Futuro con Arbitrum Stylus/rust**: Esto se implementará más adelantes con los smart contracts para que sea más escalable y pueda abordar, analizar mucho mejor la logica de los smart contracts.

## Requisitos

Para empezar a desarrollar en el proyecto, asegúrate de tener instaladas las siguientes herramientas:

- [Node.js (>= v18.18)](https://nodejs.org/en/download/)
- Yarn ([v1](https://classic.yarnpkg.com/en/docs/install/) o [v2+](https://yarnpkg.com/getting-started/install))
- [Git](https://git-scm.com/downloads)

## Guía Rápida

Para empezar a trabajar con el proyecto, sigue estos pasos en orden:

1. **Clona el repositorio y navega al directorio del proyecto**:

   ```bash
   git clone https://github.com/contratachain/contratachainfrontend.git
   cd contratachainfrontend
   ```

2. **Instala las dependencias**:

   ```bash
   yarn install
   ```

3. **Inicia la red local de Ethereum** (en una terminal):

   ```bash
   yarn chain
   ```

   Este comando inicia una red local de Ethereum utilizando Hardhat, que se usará para la prueba y desarrollo de contratos inteligentes.

4. **Despliega el contrato inteligente** (en otra terminal):

   ```bash
   yarn deploy
   ```

   Este comando despliega los contratos inteligentes definidos en la carpeta `packages/hardhat/contracts` a la red local de Ethereum.

5. **Inicia el servidor de desarrollo** (en una nueva terminal):

   ```bash
   yarn start
   ```

   Esto arrancará el frontend utilizando Next.js, y podrás acceder a la aplicación en `http://localhost:3000` para interactuar con los contratos desplegados.

Este flujo de trabajo utiliza **Scaffold-ETH 2**, que facilita la integración de contratos inteligentes con una interfaz frontend de **Next.js**. Puedes interactuar con tus contratos a través de una interfaz amigable, probar la plataforma y hacer ajustes según sea necesario.

## Desafíos y Aprendizajes

Durante el desarrollo de este proyecto, me enfrenté a varios desafíos técnicos importantes:

1. **Migración de Arbitrum Stylus**: Inicialmente intenté utilizar **Arbitrum Stylus**, que es una solución eficiente para escalabilidad en redes de blockchain. Sin embargo, me encontré con limitaciones técnicas, ya que **Hardhat** no era compatible con Stylus. A pesar de ello, aprendí mucho sobre la integración de **Stylus** en la blockchain, y estoy convencido de que en el futuro esta será una tecnología clave para el desarrollo de aplicaciones escalables.

2. **Migración de Hardhat al nodo de Arbitrum Nitro con Docker**: Decidí migrar a **Arbitrum Nitro**, que es un nodo optimizado para ser compilado y entendido por Arbitrum Stylus**Rust**.(Me ví muy tarde la clase de arbitrum Stylus) Aunque la integración de **Arbitrum Nitro** a través de **Docker** fue un desafío, me permitió avanzar en mi aprendizaje. Sin embargo, debido a mis conocimientos limitados en **Rust**, encontré dificultades técnicas que no pude resolver a tiempo.

3. **Uso de Arbitrum Sepolia**: Como ya tenía algo de conocimiento sobre **Arbitrum Sepolia** (una red que ya conozco, aunque no la desarrollé completamente debido a la falta de tiempo), opté por usar esta red para desplegar los contratos. Sin embargo, dado el tiempo limitado, decidí centrarme en el desarrollo de una **UI/UX** funcional para la plataforma, priorizando una interfaz rápida y usable para mostrar el prototipo.

A pesar de los desafíos técnicos, logré avanzar en el desarrollo de un frontend que interactúa con los contratos desplegados, proporcionando una experiencia básica de usuario.

## Cómo Contribuir

Si deseas contribuir al desarrollo del frontend, ¡nos encantaría tu ayuda! Aquí están algunos pasos para empezar:

1. **Fork del repositorio**: Realiza un fork de este repositorio y clónalo en tu máquina local.
2. **Crea una rama**: Asegúrate de crear una rama para tu nueva funcionalidad o corrección de errores.
3. **Realiza tus cambios**: Trabaja en tu rama con los cambios necesarios.
4. **Envía un pull request**: Una vez que hayas realizado los cambios, abre un pull request describiendo las modificaciones que realizaste.

*ContrataChain* Descentralizar el dinero y la información descentraliza el poder, quitandole el poder a manos corruptas.

## Documentación

Consulta la [documentación oficial](https://github.com/contratachain/contratachainFrontend) para obtener más detalles sobre cómo interactuar con la plataforma, las integraciones disponibles, y cómo personalizar el proyecto para tus necesidades.

## Licencia

Este proyecto está licenciado bajo la Licencia MIT - consulta el archivo [LICENSE](LICENSE) para más detalles.
