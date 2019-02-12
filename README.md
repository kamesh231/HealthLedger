<img src="/Static/logo/icon.png" align="left" hspace="1" vspace="1" height="150" width="150">

# Health Ledger
Application for tracking Organs donations in hospitals and minimizing the scope of Organ trafficking using Blockchain (Hyperledger) technology.

---



## The problems HealthLedger solves
Our aim is to minimize the scope of organ trafficking with the help of Blockchain technology.

- Financially weaker group sell their organs in order to get out of debt.

- Some doctors taking organs from brain dead patient without permission of their family (or without patient having signed required docs for willingly donating their organs before death).

- The records that are maintained of the organs donors and organs receiver is not secure enough and is not  transparent and could  easily be hacked or altered.

- With the help of HyperLedger we can easily dodge this issues.
  
# Instructions to run

- Clone the repo `git clone https://github.com/jogendra/HealthLedger.git`
## Running the API Backend
- Goto the API directory
- First install the [Hyperledger composer](https://hyperledger.github.io/composer/latest/installing/installing-prereqs.html). Then install the [development environment](https://hyperledger.github.io/composer/latest/installing/development-tools.html).
- `composer archive create -t dir -n .`
- `composer network install --card PeerAdmin@hlfv1 --archiveFile api@0.0.1.bna`
- `composer network start --networkName api --networkVersion 0.0.1 --card PeerAdmin@hlfv1 --networkAdmin admin --networkAdminEnrollSecret adminpw --file networkadmin.card`
- `composer card import --file networkadmin.card` 
- `composer-rest-server -c admin@api -n always -u true -d y -w true`
- Goto `http://localhost:3000/explorer` to explored the REST API

# Running the Front end
Check out: [https://jogendra.github.io/HealthLedger/](https://jogendra.github.io/HealthLedger/)
- Make sure you are running the API Backend 
- Open the `index.html` file
- The front end is up and running 

## Communication
Please join our Gitter Chanel to discuss questions regarding the project: [https://gitter.im/jogendra/HealthLedger](https://gitter.im/jogendra/HealthLedger)

## Demo
Click on the image belowe to watch the demo of the Application.
[![HealthLedger Application Demo](/Static/screenshots/1.png)](https://www.youtube.com/watch?v=yFfFxOFAh2w)


## License

This project is available under the MIT license. See the [LICENSE](LICENSE) file for more info.
