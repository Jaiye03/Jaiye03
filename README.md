!pip install diagrams # This line installs the 'diagrams' package.

from diagrams import Diagram # Imports the Diagram class from the diagrams package.
from diagrams.custom import Custom # Imports the Custom class from the diagrams.custom module.

with Diagram("Retail Stores Flowchart", show=False): # Creates a new Diagram object.
    inventory = Custom("Inventory Check", "./inventory.png") # Creates a Custom node for inventory.
    sales_order = Custom("Sales Order POS", "./sales.png") # Creates a Custom node for sales orders.
    hq = Custom("HQ Processing", "./hq.png") # Creates a Custom node for HQ processing.
    reconciliation = Custom("Cash Reconciliation", "./reconciliation.png") # Creates a Custom node for reconciliation.
    deposit = Custom("Cash Deposit", "./deposit.png") # Creates a Custom node for deposit.

    inventory >> sales_order >> hq >> reconciliation >> deposit # Defines the flow between the nodes.
