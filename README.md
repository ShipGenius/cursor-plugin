# ShipGenius for Cursor

Connects Cursor to your [ShipGenius](https://shipgeni.us) account, so you can work with your shipping data in plain words.

This repository only holds the plugin's settings. The server runs at `https://api.lite.shipgeni.us/mcp`, and there is nothing here to build or run.

## What you can do

- Ask about shipments, orders, items and inventory.
- Track packages.
- Rate shop a package across DHL eCommerce, DHL Express, FedEx, Passport Global, UniUni, UPS and USPS.
- Buy and void labels.
- Check addresses, and update orders, items and inventory.

Try asking:

- "How many labels did we buy last week, by carrier?"
- "Which orders haven't shipped yet?"
- "Rate shop a 2 lb box, 10 x 8 x 4 in, to 1100 Congress Ave, Austin, TX 78701."

## What you need

A ShipGenius Plus or OMS account. To buy labels, the account also needs prepaid credits, because labels bought this way are paid from that balance. Everything else works without them.

## Connecting

1. Install the plugin. You can also add the server yourself in `~/.cursor/mcp.json`:

    ```json
    {
        "mcpServers": {
            "shipgenius": {
                "url": "https://api.lite.shipgeni.us/mcp"
            }
        }
    }
    ```

2. In Cursor, open **Customize**, then **MCPs**, and connect ShipGenius.
3. Sign in to ShipGenius, including your second factor.
4. The consent page lists what Cursor is asking to do. Click **Approve**.

There is no API key to create and nothing to set up in ShipGenius first.

## Permissions and approvals

Cursor works as you, so it can see and do only what your ShipGenius role allows. If your role can't buy labels, Cursor can't either. Account admins can limit the connection or turn it off for the whole account from the Apps page in ShipGenius.

Cursor's default **Auto-review** mode can run a tool without asking you, and that includes a tool that buys a label. To control this, change the mode under **Cursor Settings**, then **Agents**, then **Approvals & Execution**.

## Disconnecting

In ShipGenius, go to **Connected apps** and choose **Revoke Access**, or remove the server in Cursor. Either way, Cursor loses access right away.

## More information

- [MCP guide](https://lite.shipgeni.us/developer/api-reference/mcp)
- [Privacy policy](https://lite.shipgeni.us/legal/privacy-policy)
- [Terms and conditions](https://lite.shipgeni.us/legal/terms-and-conditions)
- Support: info@shipgeni.us

## License

The files in this repository are under the [MIT License](LICENSE). The ShipGenius name and logo are not covered by it.
