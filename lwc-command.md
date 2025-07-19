1. sf project generate --name my-lwc-project -> create salesforce project

2. cd my-lwc-project

3. sf org login web --set-default -> authorize the salesforce org

3.1. sf org list  -> all the org (dev/scratch)

3.2. sf config get target-org  -> it shows which org is active

3.3. sf org delete scratch --target-org <alias-or-username>  -> to delete a target org 

4. sf org create scratch -a lwcscratch1 --duration-days 30 -f config/project-scratch-def.json  -> to create scratch dev org which is enable in salesforce env

5. sf config set target-org=lwcscratch1 -> to set a default org in Salesforce CLI

6. sf org open -o lwcscratch1 -> open the scratch org

7. sf lightning generate component --type lwc --name firstLWC --output-dir force-app/main/default/lwc  -> to create lightning component

8. sf apex generate class --name firstapex --output-dir force-app/main/default/classes -> to create apex component

9. sf project deploy start -> to push all your local source code to your scratch org 
	
10. sf project deploy start --target-org <username or alias> -> if default alias is not set
