# PACKADE-DELIVERY-SYSTEM

     #include <stdio.h>
     #include <string.h>

     struct Parcel {
    char id[20];
     };

     void main() {

    struct Parcel parcels[] = {
        {"PKG001"}, {"PKG002"}, {"PKG003"}, {"PKG100"}, {"PKG004"},
        {"PKG005"}, {"PKG006"}, {"PKG010"}, {"PKG013"}, {"PKG011"},
        {"PKG012"}, {"PKG014"}, {"PKG015"}, {"PKG016"}, {"PKG017"},
        {"PKG018"}, {"PKG019"}, {"PKG020"}
    };

    int parcel_count = sizeof(parcels) / sizeof(parcels[0]);

    int n;
    printf("Enter the number of parcels to be searched: ");
    scanf("%d", &n);

    char search_id[20];

    for (int i = 0; i < n; i++) {

        printf("\nEnter Parcel ID to search: ");
        scanf("%s", search_id);

        int found = 0;

        for (int j = 0; j < parcel_count; j++) {
            if (strcmp(parcels[j].id, search_id) == 0) {
                found = 1;
                break;
            }
        }

        if (found == 1) {
            printf("Parcel FOUND in the system. PARCEL IS OUT FOR DELIVERY\n");
        } else {
            printf("Parcel NOT FOUND. PARCEL IS ALREADY DELIVERED\n");
        }
    }

    }
